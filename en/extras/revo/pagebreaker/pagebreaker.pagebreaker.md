---
title: "PageBreaker.PageBreaker"
_old_id: "944"
_old_uri: "revo/pagebreaker/pagebreaker.pagebreaker"
---

<div>- [Description](#PageBreaker.PageBreaker-Description)
- [Properties](#PageBreaker.PageBreaker-Properties)
- [See Also](#PageBreaker.PageBreaker-SeeAlso)

</div>Description
-----------

Plugin have two modes of work.

- **OnLoadWebDocument** - searching for strings **<!-- splitter -->** in content, splits text on pages and generating pagination using chunk [tpl.PageBreaker.navigation](/extras/revo/pagebreaker/tpl.pagebreaker.navigation "tpl.PageBreaker.navigation")
- **OnPageNotFound** - searching resource by generated url of page and loads it.

Properties
----------

- pb\_ajax - enable changing pages trought ajax? By default: no. See chunk [tpl.PageBreaker.ajax](/extras/revo/pagebreaker/tpl.pagebreaker.ajax "tpl.PageBreaker.ajax")
- pb\_load\_jquery - need to include jquery library? By default: no.

<div class="info">I do not recommend to enable ajax mode in due to decreasing count of pages hits and worse indexing this pages by crawlers. Also it is complicate users to bookmark reading page.</div>See Also
--------

1. [PageBreaker.PageBreaker](/extras/revo/pagebreaker/pagebreaker.pagebreaker)
2. [tpl.PageBreaker.ajax](/extras/revo/pagebreaker/tpl.pagebreaker.ajax)
3. [tpl.PageBreaker.navigation](/extras/revo/pagebreaker/tpl.pagebreaker.navigation)