---
title: "eventsCalendar2.tplEvent2"
_old_id: "838"
_old_uri: "revo/eventscalendar2/eventscalendar2.tplevent2"
---

<div>- [Usage](#eventsCalendar2.tplEvent2-Usage)
- [Placeholders](#eventsCalendar2.tplEvent2-Placeholders)
- [See Also](#eventsCalendar2.tplEvent2-SeeAlso)

</div>Usage
-----

This chunk is a template for one event in the day.

```
<pre class="brush: php">
<div><div>
        <span class="num"><b>[[+ec.num]].</b></span>
        <span class="eventdate">[[+ec.date]]</span>
        <span class="link"><a href="[[+ec.url]]">[[+ec.longtitle:default=`[[+ec.pagetitle]]`]]</a></span>
        <span class="notice">[[+ec.introtext]]</span>
</div>

```Placeholders
------------

<table><tbody><tr><th>Name</th><th>Description</th></tr><tr><td>num</td><td>Number of event in day.</td></tr><tr><td>url</td><td>Link to resource of this event.</td></tr><tr><td>date</td><td>Date of event.</td></tr></tbody></table>You can use all placeholders from MODx resources. See it [there](http://rtfm.modx.com/display/revolution20/Resources).

If you displaying events from custom source (param &events=``) all properties in events array will be converted to placeholders.

See Also
--------

1. [eventsCalendar2.eventsCalendar2](/extras/revo/eventscalendar2/eventscalendar2.eventscalendar2)
2. [eventsCalendar2.Generating events](/extras/revo/eventscalendar2/eventscalendar2.generating-events)
3. [eventsCalendar2.tplCalendar2](/extras/revo/eventscalendar2/eventscalendar2.tplcalendar2)
4. [eventsCalendar2.tplCell2](/extras/revo/eventscalendar2/eventscalendar2.tplcell2)
5. [eventsCalendar2.tplEvent2](/extras/revo/eventscalendar2/eventscalendar2.tplevent2)
6. [eventsCalendar2.tplHead2](/extras/revo/eventscalendar2/eventscalendar2.tplhead2)