---
title: target
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Event
    href: /dom/Event
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets the element that is the original target of the event.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/target

---
## Summary

Gets the element that is the original target of the event.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var originalTargetElement = event.target;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The original target element of the event.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine the original element on which the event was dispatched.

## Notes

The [**currentTarget**](/dom/Event/currentTarget) property returns the element that the event handlers are being processed for during the capturing and bubbling phases.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages (MSDN)

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
