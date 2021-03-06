---
title: "Quip.Quip.tplComments"
_old_id: "960"
_old_uri: "revo/quip/quip.quip/quip.quip.tplcomments"
---

Quip's tplComments Chunk
------------------------

This is the Chunk displayed with the &tplComments property on the [Quip.Quip](/extras/revo/quip/quip.quip "Quip.Quip") snippet. Only applicable when &useWrapper is set to 1 in the Quip snippet (which it is by default).

This chunk wraps the comments for a thread, and provides a heading with the total number of comments.

Default Value
-------------

```
<pre class="brush: php">
<div class="quip">
    <h3>[[%quip.comments]] ([[+total]])</h3>
        
    <div id="quip-topofcomments-[[+idprefix]]"></div>

    [[+comments:notempty=`<ol class="quip-comment-list">
    [[+comments]]
    </ol>`]]

    [[+pagination]]
</div>

```Available Placeholders
----------------------

<table><tbody><tr><th>Name</th><th>Description</th></tr><tr><td>comments</td><td>The comments for the thread.</td></tr><tr><td>total</td><td>The total number of comments for this thread.</td></tr><tr><td>idprefix</td><td>The ID prefix for the thread's comments.</td></tr></tbody></table>See Also
--------

1. [Quip.Quip](/extras/revo/quip/quip.quip)
  1. [Quip.Quip.tplComment](/extras/revo/quip/quip.quip/quip.quip.tplcomment)
  2. [Quip.Quip.tplCommentOptions](/extras/revo/quip/quip.quip/quip.quip.tplcommentoptions)
  3. [Quip.Quip.tplComments](/extras/revo/quip/quip.quip/quip.quip.tplcomments)
  4. [Quip.Quip.tplReport](/extras/revo/quip/quip.quip/quip.quip.tplreport)
2. [Quip.QuipCount](/extras/revo/quip/quip.quipcount)
3. [Quip.QuipLatestComments](/extras/revo/quip/quip.quiplatestcomments)
4. [Quip.QuipReply](/extras/revo/quip/quip.quipreply)
  1. [Quip.QuipReply.tplAddComment](/extras/revo/quip/quip.quipreply/quip.quipreply.tpladdcomment)
  2. [Quip.QuipReply.tplLoginToComment](/extras/revo/quip/quip.quipreply/quip.quipreply.tpllogintocomment)
  3. [Quip.QuipReply.tplPreview](/extras/revo/quip/quip.quipreply/quip.quipreply.tplpreview)
5. [Quip.QuipRss](/extras/revo/quip/quip.quiprss)
6. [Quip.Roadmap](/extras/revo/quip/quip.roadmap)
7. [Quip.Upgrading](/extras/revo/quip/quip.upgrading)
  1. [Quip.Upgrading to 1.0.1](/extras/revo/quip/quip.upgrading/quip.upgrading-to-1.0.1)