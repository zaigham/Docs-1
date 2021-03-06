---
title: "modX.getLoginUserName"
_old_id: "1067"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.getloginusername"
---

modX::getLoginUserName
----------------------

Returns the current user name, for the current or specified context.

Syntax
------

API Doc: [http://api.modx.com/revolution/2.2/db\_core\_model\_modx\_modx.class.html#%5CmodX::getLoginUserName()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::getLoginUserName())

```
<pre class="brush: php">
string getLoginUserName ([string $context = ''])

```Example
-------

Grab the user's username in the current Context.

```
<pre class="brush: php">
$username = $modx->getLoginUserName();

```See Also
--------

- [Contexts](/revolution/2.x/administering-your-site/contexts "Contexts")