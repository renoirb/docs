---
title: timeStamp
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Event
    href: /dom/Event
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets the time, in milliseconds, when an event occurred.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/timeStamp

---
## Summary

Gets the time, in milliseconds, when an event occurred.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var eventTimestamp = event.timeStamp;
```

## Return Value

Returns an object of type NumberNumber

The event time stamp, in milliseconds since 1970-1-1 00:00:00 UTC.

## Examples

The following event handler displays the event time by using the current locale settings.

``` js
function eventHandler(evt) {
    var dt = new Date(evt.timeStamp);
    alert(dt.toLocaleString());
}
window.onload = eventHandler;
```

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages

-   `SVGZoomEvent`
-   `BeforeUnloadEvent`
-   `CompositionEvent`
-   `CustomEvent`
-   `DragEvent`
-   `Event`
-   `FocusEvent`
-   `KeyboardEvent`
-   `MessageEvent`
-   `MouseEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
