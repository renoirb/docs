---
title: fillText
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
summary: 'Renders the given text at the given (x, y) coordinates, ensuring that the text isn''t wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/fillText

---
## <span>Summary</span>

Renders the given text at the given (x, y) coordinates, ensuring that the text isn't wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.fillText(text, x, y, maxWidth);
```

## <span>Parameters</span>

### <span>text</span>

 Data-type
:   String

 The text characters to paint on the canvas.

### <span>x</span>

 Data-type
:   Number

 The horizontal coordinate to start painting the text at, relative to the canvas.

### <span>y</span>

 Data-type
:   Number

 The vertical coordinate to start painting the text, relative to the canvas.

### <span>maxWidth</span>

 Data-type
:   Number

(Optional)

The maximum possible text width. If the value is less than the [width](/apis/canvas/TextMetrics/width) property, the text is scaled to fit.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|SecurityError|The current font is not of the same origin or domain as the document that owns the canvas element.|

## <span>Examples</span>

This example sets a font for upcoming text, then places the value of a string variable onto the canvas.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var text = "Hello, world.";
ctxt.font="24px Verdana";
ctxt.fillText(text, 50, 75);
</script>
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
