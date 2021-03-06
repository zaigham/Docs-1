---
title: "SimpleSearch.SimpleSearchForm.tpl"
_old_id: "1003"
_old_uri: "revo/simplesearch/simplesearch.simplesearchform/simplesearch.simplesearchform.tpl"
---

SimpleSearchForm's tpl Chunk
----------------------------

This is the Chunk displayed with the &tpl property on the [SimpleSearch](/extras/revo/simplesearch/simplesearch.simplesearchform "SimpleSearch.SimpleSearchForm") snippet.

Default Value
-------------

```
<pre class="brush: php">
<form class="sisea-search-form" action="[[~[[+landing:default=`[[*id]]`]]]]" method="[[+method:default=`get`]]">
  <fieldset>
    <label for="[[+searchIndex]]">[[%sisea.search? &namespace=`sisea` &topic=`default`]]</label>
    <input type="text" name="[[+searchIndex]]" id="[[+searchIndex]]" value="[[+searchValue]]" />
    <input type="hidden" name="id" value="[[+landing:default=[[*id]]]]" /> 
    <input type="submit" value="[[%sisea.search? &namespace=`sisea` &topic=`default`]]" />
  </fieldset>
</form>

```Available Placeholders
----------------------

<table><tbody><tr><th>Name</th><th>Description</th></tr><tr><td>landing</td><td>The ID of the Resource to show search results on. Defaults to the current Resource.</td></tr><tr><td>method</td><td>Whether to submit over GET or POST. Defaults to GET.</td></tr><tr><td>searchValue</td><td>The current search value. Defaults blank unless a prior search has been performed.</td></tr><tr><td>searchIndex</td><td>The REQUEST var used for the search parameter.</td></tr></tbody></table>See Also
--------

1. [SimpleSearch.Roadmap](/extras/revo/simplesearch/simplesearch.roadmap)
2. [SimpleSearch.SimpleSearch](/extras/revo/simplesearch/simplesearch.simplesearch)
  1. [SimpleSearch.SimpleSearch.containerTpl](/extras/revo/simplesearch/simplesearch.simplesearch/simplesearch.simplesearch.containertpl)
  2. [SimpleSearch.SimpleSearch.currentPageTpl](/extras/revo/simplesearch/simplesearch.simplesearch/simplesearch.simplesearch.currentpagetpl)
  3. [SimpleSearch.SimpleSearch.pageTpl](/extras/revo/simplesearch/simplesearch.simplesearch/simplesearch.simplesearch.pagetpl)
  4. [SimpleSearch.SimpleSearch.tpl](/extras/revo/simplesearch/simplesearch.simplesearch/simplesearch.simplesearch.tpl)
  5. [SimpleSearch.Faceted Search Through PostHooks](/extras/revo/simplesearch/simplesearch.simplesearch/simplesearch.faceted-search-through-posthooks)
3. [SimpleSearch.SimpleSearchForm](/extras/revo/simplesearch/simplesearch.simplesearchform)
  1. [SimpleSearch.SimpleSearchForm.tpl](/extras/revo/simplesearch/simplesearch.simplesearchform/simplesearch.simplesearchform.tpl)
4. [SimpleSearch.Solr](/extras/revo/simplesearch/simplesearch.solr)