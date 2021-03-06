---
title: "EventsX.Examples"
_old_id: "840"
_old_uri: "revo/eventsx/eventsx.examples"
---

<div>- [Examples for EventsX](#EventsX.Examples-ExamplesforEventsX)
  - [Display a list of upcoming events](#EventsX.Examples-Displayalistofupcomingevents)
  - [create your chunk "upcomingEvents":](#EventsX.Examples-createyourchunk%22upcomingEvents%22%3A)
  - [create snippet call](#EventsX.Examples-createsnippetcall)
  - [screenshot](#EventsX.Examples-screenshot)
- [See Also](#EventsX.Examples-SeeAlso)

</div>Examples for EventsX
--------------------

### Display a list of upcoming events

Go to components -> EventsX and create some events

(make sure they are active)

### create your chunk "upcomingEvents":

```
<pre class="brush: php">
        <li>[[+location:htmlentities]]: <a href="[[+url]]" title="[[+name:htmlentities]]">[[+name:htmlentities]]</a> <time datetime="[[+startdate:strtotime:date=`%Y-%m-%d`]]" title="event is scheduled on [[+startdate:strtotime:date=`%d.%m.%Y`]]">[[+startdate:strtotime:date=%d.%m.%Y`]]</time></li>

```### create snippet call

Add this snippet call on your template or resource where you would like to display the list of events.

```
<pre class="brush: php">
        <h2>next events:</h2>
        <ol id="eventcal">
                [[!EventsX? &tpl=`upcomingEvents` &limit=`10`]]
        </ol>

```### screenshot

A screenshot could look like this. Note that I've styled the time element individually.

![](/download/attachments/37683422/eventsx.png?version=1&modificationDate=1326443860000)

See Also
--------

1. [EventsX.Examples](/extras/revo/eventsx/eventsx.examples)