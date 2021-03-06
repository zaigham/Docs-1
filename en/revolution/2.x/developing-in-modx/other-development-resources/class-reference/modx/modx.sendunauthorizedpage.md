---
title: "modX.sendUnauthorizedPage"
_old_id: "1104"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.sendunauthorizedpage"
---

modX::sendUnauthorizedPage
--------------------------

 Send the user to the MODx unauthorized page.

Syntax
------

 API Doc: [http://api.modx.com/revolution/2.2/db\_core\_model\_modx\_modx.class.html#%5CmodX::sendUnauthorizedPage()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::sendUnauthorizedPage())

 ```
<pre class="brush: php">
void sendUnauthorizedPage ([array $options = null])

```Example
-------

 Send the user to the unauthorized page. You do not need to terminate the script after running this.

 ```
<pre class="brush: php">
$modx->sendUnauthorizedPage();

```See Also
--------

- [modX](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx "modX")
- [modX.sendErrorPage](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.senderrorpage "modX.sendErrorPage")
- [modX.sendForward](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.sendforward "modX.sendForward")
- [modX.sendRedirect](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.sendredirect "modX.sendRedirect")