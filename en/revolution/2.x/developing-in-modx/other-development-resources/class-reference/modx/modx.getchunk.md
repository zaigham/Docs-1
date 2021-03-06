---
title: "modX.getChunk"
_old_id: "1062"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.getchunk"
---

modX::getChunk
--------------

Processes and returns the output from an HTML chunk by name.

**getChunk** actually sets the properties you pass (and that are picked up from default properties and/or a property set) as placeholders (preserving any with the same key and restoring those after processing is complete) and allows the modChunk class to process() them (along with any other tags, filters, etc.).

<div class="info">**getChunk** will execute the MODX parser, so you can use output filters and the $properties array can be multi-dimenstional (i.e. more than just simple key/value pairs). If this is more horsepower than you need, use [modX.parseChunk](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.parsechunk "modX.parseChunk") instead.</div>Syntax
------

API Doc: [http://api.modx.com/revolution/2.2/db\_core\_model\_modx\_modx.class.html#%5CmodX::getChunk()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::getChunk())

```
<pre class="brush: php">
string getChunk (string $chunkName, [array $properties = array ()])

```**$properties** is usually a standard associative array, e.g.

```
<pre class="brush: php">
$properties = array('key' => 'value');

```Which would cause the \[\[+key\]\] placeholders to be replaced by the 'value'.

However, **$properties** can also be a more deeply nested array such as the kind that might be returned from certain getObject or getCollection queries, e.g.

```
<pre class="brush: php">
$properties = array(
    'user' => array('id' => 1),
    'document' => array('id' => 27)
);
// or:
$properties['user']['id'] = 1;
$properties['document']['id'] = 27;

// Corresponds to the following placeholders:
// [[+user.id]]
// [[+document.id]]

```In cases where a multi-dimensional array is used, the placeholder syntax changes to use a dot for each node in the array, e.g. \[\[+user.id\]\] and \[\[+document.id\]\]

Examples
--------

### Simple Example

Lets process this chunk and output its value. We have this Chunk, called "WelcomeChunk":

```
<pre class="brush: php">
<p>Welcome [[+name]]!</p>

```We'll put this in our Snippet:

```
<pre class="brush: php">
$output = $modx->getChunk('WelcomeChunk',array(
   'name' => 'John',
));
return $output;

```So every key in the associative array passed to the **getChunk** method corresponds to an available placeholder inside the chunk, e.g. \[\[+name\]\]

This code outputs this:

```
<pre class="brush: php">
<p>Welcome John!</p>

```### Nested $properties

In our Chunk:

```
<pre class="brush: php">
<a href="http://site.com/profile?user_id=[[+user.id]]!">User Details</a>

```In our Snippet:

```
<pre class="brush: php">
$output = $modx->getChunk('UserLink',array(
   'user' => array('id' => 123)
);
return $output;

```### Used in a Snippet

Often, MODX Chunks are used as [formatting string](http://php.net/manual/en/function.sprintf.php) by Snippets. To that end, you can make good use of xPDO's [toArray()](/xpdo/2.x/class-reference/xpdoobject/field-accessors/toarray "toArray") method.

Imagine a Chunk named **single\_user**:

```
<pre class="brush: php">
Username: [[+username]]<br/>
Active?:  [[+active]]<br/>
<hr/>

```Then in your Snippet:

```
<pre class="brush: php">
$userlist = $modx->getCollection('modUser');

$output = '';
foreach ($userlist as $user) {
    $output .= $modx->getChunk('single_user', $user->toArray() );
}

return $output;

```### Parsing a String

Sometimes you need to parse a string using the MODX parser – this does not use getChunk, but it is related. Using the MODX parser is a bit slower than using a simple str\_replace function, but it does let you use complex placeholders (e.g. to include another Chunk) and output filters etc. The trick is to create a temporary Chunk object, then run the **process** method on it.

```
<pre class="brush: php">
// The formatting String
$tpl = 'Hello, my name is [[+name]]';

// Properties
$props = array('name' => 'Bob');

// Create the temporary chunk
$uniqid = uniqid();
$chunk = $modx->newObject('modChunk', array('name' => "{tmp}-{$uniqid}"));
$chunk->setCacheable(false);

$output = $chunk->process($props, $tpl);

```See Also
--------

- [Chunks](/revolution/2.x/making-sites-with-modx/structuring-your-site/chunks "Chunks")
- [modX.parseChunk](/revolution/2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.parsechunk "modX.parseChunk")