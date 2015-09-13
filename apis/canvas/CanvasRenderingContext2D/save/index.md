---
title: save
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
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
summary: 'Saves the current state of the context. Use the restore() method to retrieve the saved state.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/save

---
## <span>Summary</span>

Saves the current state of the context. Use the restore() method to retrieve the saved state.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.save();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.rect(50,50,125,75);
ctxt.stroke();
ctxt.save();
ctxt.restore();
</script>
```

## <span>Notes</span>

The *save* and [restore](/apis/canvas/CanvasRenderingContext2D/restore) methods preserve and restore the state of a context, but not specific paths or graphics. The following attributes and states are affected:

-   The current transformation matrix
-   The current clipping region
-   The current values of the following attributes:
    -   *strokeStyle*
    -   *fillStyle*
    -   *globalAlpha*
    -   *lineWidth*
    -   *lineCap*
    -   *lineJoin*
    -   *miterLimit*

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
