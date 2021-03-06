---
title: "xPDO.getManager"
_old_id: "1587"
_old_uri: "1.x/class-reference/xpdo/xpdo.getmanager"
---

xPDO::getManager
----------------

Gets the manager class for this xPDO connection.

The manager class can perform operations such as creating or altering table structures, creating data containers, generating custom persistence classes, and other advanced operations that do not need to be loaded frequently.

Syntax
------

API Docs: <http://api.modxcms.com/xpdo/xPDO.html#getManager>

```
<pre class="brush: php">
object|null getManager ()

```Example
-------

```
<pre class="brush: php">
$manager = $xpdo->getManager();

```See Also
--------

- [xPDOManager](/xpdo/1.x/class-reference/xpdomanager "xPDOManager")
- [xPDO](/xpdo/1.x/class-reference/xpdo "xPDO")