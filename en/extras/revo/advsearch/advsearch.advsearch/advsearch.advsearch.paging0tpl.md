---
title: "AdvSearch.AdvSearch.paging0Tpl"
_old_id: "769"
_old_uri: "revo/advsearch/advsearch.advsearch/advsearch.advsearch.paging0tpl"
---

AdvSearch's paging0Tpl Chunk
----------------------------

A Chunk named "**Paging0**" is provided with AdvSearch. This Chunk name is set as &paging0Tpl property on the [AdvSearch](/extras/revo/advsearch/advsearch.advsearch "AdvSearch.AdvSearch")AdvSearch snippet.

Default Value
-------------

```
<pre class="brush: php">
<span class="advsea-result-pages">[[%advsearch.result_pages? &namespace=`advsearch` &topic=`default`]]</span>[[+paging0]]

```Available Placeholders
----------------------

<table><tbody><tr><th>Name</th><th>Description</th></tr><tr><td>paging0</td><td>The pagination.</td></tr></tbody></table>AdvSearch's pageTpl and CurrentPageTpl Chunks
---------------------------------------------

Two Chunks named "**PageLink**" and "**CurrentPageLink**" are provided to set up the paging type 0.   
These Chunk names are set as &pageTpl and &currentPageTpl properties on the [AdvSearch](/extras/revo/advsearch/advsearch.advsearch "AdvSearch.AdvSearch") snippet.

Default Value for PageLink
--------------------------

```
<pre class="brush: php">
<span class="advsea-page"><a href="[[+link]]">[[+text]]</a></span>

```Default Value for CurrentPageLink
---------------------------------

```
<pre class="brush: php">
<span class="advsea-page advsea-current-page">[[+text]]</span>

```Available Placeholders
----------------------

<table><tbody><tr><th>Name</th><th>Description</th></tr><tr><td>link</td><td>The link to the page</td></tr><tr><td>text</td><td>The page number</td></tr></tbody></table>You could define the separator between page link numbers by using the pagingSeparator parameter.

See Also
--------

1. [AdvSearch.AdvSearch](/extras/revo/advsearch/advsearch.advsearch)
  1. [AdvSearch.AdvSearch.containerTpl](/extras/revo/advsearch/advsearch.advsearch/advsearch.advsearch.containertpl)
  2. [Advsearch.AdvSearch.extractTpl](/extras/revo/advsearch/advsearch.advsearch/advsearch.advsearch.extracttpl)
  3. [AdvSearch.Advsearch.paging1Tpl](/extras/revo/advsearch/advsearch.advsearch/advsearch.advsearch.paging1tpl)
  4. [AdvSearch.AdvSearch.paging0Tpl](/extras/revo/advsearch/advsearch.advsearch/advsearch.advsearch.paging0tpl)
  5. [AdvSearch.AdvSearch.tpl](/extras/revo/advsearch/advsearch.advsearch/advsearch.advsearch.tpl)
2. [AdvSearch.AdvSearchForm](/extras/revo/advsearch/advsearch.advsearchform)
  1. [Advsearch.AdvSearchForm.tpl](/extras/revo/advsearch/advsearch.advsearchform/advsearch.advsearchform.tpl)
3. [AdvSearch.AdvSearchHelp](/extras/revo/advsearch/advsearch.advsearchhelp)
  1. [AdvSearch.AdvSearchHelp.helplinkTpl](/extras/revo/advsearch/advsearch.advsearchhelp/advsearch.advsearchhelp.helplinktpl)