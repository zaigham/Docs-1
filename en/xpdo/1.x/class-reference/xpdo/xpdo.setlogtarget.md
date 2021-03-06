---
title: "xPDO.setLogTarget"
_old_id: "1597"
_old_uri: "1.x/class-reference/xpdo/xpdo.setlogtarget"
---

xPDO::setLogTarget
------------------

 Sets the log target for xPDO::\_log() calls.

 Valid target values include:

- 'ECHO': Returns output to the STDOUT.
- 'HTML': Returns output to the STDOUT with HTML formatting.
- 'FILE': Sends output to a log file.
- An array with at least one element with key 'target' matching one of the valid log targets listed above. For 'target' => 'FILE' you can specify a second element with key 'options' with another associative array with one or both of the elements 'filename' and 'filepath'.

Syntax
------

 API Docs: <http://api.modxcms.com/xpdo/xPDO.html#setLogTarget>

 ```
<pre class="brush: php">
void setLogTarget ([string $target = 'ECHO'], mixed 1)

```Examples
--------

 Set the log target to format log messages in HTML and output to the browser.

 ```
<pre class="brush: php">
$xpdo->setLogTarget('HTML');

``` Set the log target to output anything WARN or above to a new log file that is set with 'install.' plus a timestamp of current execution (useful for install procedures).

 ```
<pre class="brush: php">
$xpdo->setLogLevel(xPDO_LOG_LEVEL_WARN);
$xpdo->setLogTarget(array(
   'target' => 'FILE',
   'options' => array(
       'filename' => 'install.' . strftime('%Y-%m-%dT%H:%M:%S')
    )
));

```See Also
--------

- [xPDO](/xpdo/1.x/class-reference/xpdo "xPDO")
- [xPDO.log](/xpdo/2.x/class-reference/xpdo/xpdo.log)