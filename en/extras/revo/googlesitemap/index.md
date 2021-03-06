---
title: "GoogleSiteMap"
_old_id: "656"
_old_uri: "revo/googlesitemap/"
---

<div>- [What is GoogleSiteMap?](#GoogleSiteMap-WhatisGoogleSiteMap%3F)
- [Requirements](#GoogleSiteMap-Requirements)
- [History and Info](#GoogleSiteMap-HistoryandInfo)
  - [Download](#GoogleSiteMap-Download)
  - [Development and Bug Reporting](#GoogleSiteMap-DevelopmentandBugReporting)
- [Usage](#GoogleSiteMap-Usage)
  - [Snippets](#GoogleSiteMap-Snippets)
- [Examples](#GoogleSiteMap-Examples)
- [See Also](#GoogleSiteMap-SeeAlso)
 
</div>What is GoogleSiteMap?
----------------------

 GoogleSiteMap is a snippet that will display a Google-customized SiteMap for your site.

Requirements
------------

- MODx Revolution 2.2.x or later
- PHP5.4 or later

History and Info
----------------

 In 2016 GoogleSiteMap was completely re-written by YJ Tso (@sepiariver) based on blazing-fast sitemap code by Garry Nutting (@garryn), after it was found that the legacy Snippet would time-out when more than several thousand nodes needed to be generated.

 The trade-off was that some of the legacy features could not be supported. An attempt was made to maintain backwards compatibility, by calling the legacy Snippet if a legacy feature is required.

 The legacy GoogleSiteMap Snippet was originally written by Shaun McCormick (splittingred) as a Snippet to display a Google SiteMap, and first released on June 23rd, 2009.

 You can view the [roadmap here](/extras/revo/googlesitemap/googlesitemap.roadmap "GoogleSiteMap.Roadmap").

### Download

 It can be downloaded from within the MODx Revolution manager via <span class="error">\[Package Management\]</span>, or from the MODx Extras Repository, available here: <https://modx.com/extras/package/googlesitemap>

### Development and Bug Reporting

 GoogleSiteMap source code is managed in GitHub, and can be found here: <http://github.com/modxcms/GoogleSiteMap>

Usage
-----

 GoogleSiteMap can be called via the Snippet tags.

### Snippets

 GoogleSiteMap comes with two snippets:

- [GoogleSiteMap](/extras/revo/googlesitemap/googlesitemap.googlesitemap "GoogleSiteMap.GoogleSiteMap")
- [GoogleSiteMapVersion1](https://rtfm.modx.com/extras/revo/googlesitemap/googlesitemapversion1)

Examples
--------

 Display a Google SiteMap for tens of thousands of Resources.

 ```
<pre class="brush: php">
[[!GoogleSiteMap]]

``` Display a Google SiteMap for a more modest number of Resources, using a custom item template Chunk.

 ```
<pre class="brush: php">
[[!GoogleSiteMap? &itemTpl=`myCustomTpl`]]

```<div class="warning"> Note: the latter example would result in the legacy Snippet being called and will time-out if a huge number of nodes need to be generated. </div>See Also
--------

1. [GoogleSiteMap.GoogleSiteMap](/extras/revo/googlesitemap/googlesitemap.googlesitemap)
  1. [GoogleSiteMap.GoogleSiteMap.containerTpl](/extras/revo/googlesitemap/googlesitemap.googlesitemap/googlesitemap.googlesitemap.containertpl)
  2. [GoogleSiteMap.GoogleSiteMap.itemTpl](/extras/revo/googlesitemap/googlesitemap.googlesitemap/googlesitemap.googlesitemap.itemtpl)
2. [GoogleSiteMapVersion1](https://rtfm.modx.com/extras/revo/googlesitemap/googlesitemapversion1)
3. [GoogleSiteMap.Roadmap](/extras/revo/googlesitemap/googlesitemap.roadmap)