---
title: "tpl.PageBreaker.ajax"
_old_id: "1026"
_old_uri: "revo/pagebreaker/tpl.pagebreaker.ajax"
---

<div>- [Description](#tpl.PageBreaker.ajax-Description)
- [Placeholders](#tpl.PageBreaker.ajax-Placeholders)
- [See Also](#tpl.PageBreaker.ajax-SeeAlso)

</div>Description
-----------

This chunk used only if you enable **pb\_ajax** parameter of [PageBreaker](/extras/revo/pagebreaker/pagebreaker.pagebreaker "PageBreaker.PageBreaker") plugin.

It is simply handle clicks on links with class **load\_page** and sends ajax request to current page. After receiving response from plugin it changes old text block to new.

You need to specify id of element on webpage where content is.

```
<pre class="brush: php">
<script type='text/javascript'>
  var elem = '#content'; // HTML element on webpage in which will be loaded new block of text

  $(document).ready(function() {
    $('.load_page').live('click', function() {
      var href = $(this).attr('href');
      $.post(href, {'action': 'PageBreakLoad'}, function(data) {
              $(elem).html(data);
      })
      return false;
    })
  })

</script>

```Placeholders
------------

There is no unusual placeholders in this chunk.

See Also
--------

1. [PageBreaker.PageBreaker](/extras/revo/pagebreaker/pagebreaker.pagebreaker)
2. [tpl.PageBreaker.ajax](/extras/revo/pagebreaker/tpl.pagebreaker.ajax)
3. [tpl.PageBreaker.navigation](/extras/revo/pagebreaker/tpl.pagebreaker.navigation)