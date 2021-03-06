---
title: "modX.getSessionState"
_old_id: "1076"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.getsessionstate"
---

modX::getSessionState
---------------------

Returns the state of the SESSION being used by modX.

The possible values for session state are:

- modX::SESSION\_STATE\_UNINITIALIZED
- modX::SESSION\_STATE\_UNAVAILABLE
- modX::SESSION\_STATE\_EXTERNAL
- modX::SESSION\_STATE\_INITIALIZED

Syntax
------

API Doc: [http://api.modx.com/revolution/2.2/db\_core\_model\_modx\_modx.class.html#%5CmodX::getSessionState()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::getSessionState())

```
<pre class="brush: php">
integer getSessionState ()

```Example
-------

```
<pre class="brush: php">
$state = $modx->getSessionState();

```See Also
--------

- [modX](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx "modX")