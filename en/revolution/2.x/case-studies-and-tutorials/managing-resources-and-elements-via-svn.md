---
title: "Managing Resources and Elements via SVN"
_old_id: "195"
_old_uri: "2.x/case-studies-and-tutorials/managing-resources-and-elements-via-svn"
---

The Problem
-----------

 When working in collaboration, teams of developers and designers often collaborate via Subversion (SVN) to make development easier between multiple people. MODx, however, stores its data in the database. This has many benefits generally, but DB-stored code cannot be version-controlled via SVN.

 However, the solution in MODx Revolution is quite simple.

The Solution
------------

 For Resources, it's simple. Just use [Static Resources](/revolution/2.x/making-sites-with-modx/structuring-your-site/resources/static-resource "Static Resource"), and point the content to a file in your SVN checkout.

<div class="note"> The following is relevant to older versions of MODX. For MODX 2.2.x, as with static resources, simply use [Static Elements](/revolution/2.x/administering-your-site/upgrading-modx/upgrading-to-2.2.x#Upgradingto2.2.x-StaticElements). Static Elements have the further advantage of being able to use [Media Sources](/revolution/2.x/administering-your-site/upgrading-modx/upgrading-to-2.2.x#Upgradingto2.2.x-MediaSources). </div> For Elements, all you need is a simple "include" [snippet](/revolution/2.x/developing-in-modx/basic-development/snippets "Snippets"). The code:

 ```
<pre class="brush: php">
if (!file_exists($file)) return '';
$o = include $file;
return $o;

``` You can then call it like so in your Static Resources:

 ```
<pre class="brush: php">
[[include? &file=`/path/to/my/svn/checkout/snippet.php`]]

``` And you're done. You can also use tags within the 'file' parameter, such as this:

 ```
<pre class="brush: php">
[[include? &file=`[[++assets_path]]/js/myscript.js`]]

```Conclusion
----------

 This allows you to easily manage content via SVN. It can be achieved with [Templates](/revolution/2.x/making-sites-with-modx/structuring-your-site/templates "Templates") and [TVs](/revolution/2.x/making-sites-with-modx/customizing-content/template-variables "Template Variables") as well; just plop the include snippet wherever you need filesystem-based files.