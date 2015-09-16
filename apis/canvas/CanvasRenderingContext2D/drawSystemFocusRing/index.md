---
title: drawSystemFocusRing
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Removed from spec; deletion candidate.'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: "Draws a focus ring of the appropriate style along the intended path, following platform conventions.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/drawSystemFocusRing

---
## Summary

Draws a focus ring of the appropriate style along the intended path, following platform conventions.

**Removed from spec; deletion candidate.**

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.drawSystemFocusRing(path, element);
```

## Parameters

### path

 Data-type
:   DOM Node

(Optional)

The path along which the focus ring is to be drawn.

### element

 Data-type
:   DOM Node

 The element on which the focus ring is to be drawn.

## Return Value

Returns an object of type DOM NodeDOM Node

**Needs Examples**: This section should include examples.

## Notes

The focus ring should not be subject to the shadow effects, the global alpha, or the global composition operators, but should be subject to the clipping region.

## Related specifications

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
