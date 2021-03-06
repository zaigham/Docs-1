---
title: "xPDO.getFields"
_old_id: "1586"
_old_uri: "1.x/class-reference/xpdo/xpdo.getfields"
---

xPDO::getFields
---------------

Gets a list of fields (or columns) for an object by class name.

This includes default values for each field and is used by the objects themselves to build their initial attributes based on class inheritence.

Syntax
------

API Docs: <http://api.modxcms.com/xpdo/xPDO.html#getFields>

```
<pre class="brush: php">
array getFields (string $className)

```Example
-------

Get a list of fields for the Box object, which has 3 fields: id, width and height:

```
<pre class="brush: php">
$fields = $xpdo->getFields('Box');
print_r($fields); // prints: Array ([id] => 1, [width] => 10, [height] => 23)

```See Also
--------

- [xPDO](/xpdo/1.x/class-reference/xpdo "xPDO")