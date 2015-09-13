---
title: font
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'The current canvas context font and characteristics, in the manner of the CSS font property.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/font

---
## <span>Summary</span>

The current canvas context font and characteristics, in the manner of the CSS font property.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var result = CanvasRenderingContext2D.font;
CanvasRenderingContext2D.font = value;
```

## <span>Return Value</span>

Returns an object of type StringString

The font string can consist of any CSS font description and is analogous to the CSS *font* property. The default font is `10px sans-serif`. Values that are not CSS font values are ignored.

## <span>Examples</span>

The following exaple write a sample string in the canvas

``` js
function draw() {
  var ctx = document.getElementById('MyCanvas').getContext('2d');

  ctx.font = "16px Times New Roman";
  ctx.fillText("Lorem ipsum", 0, 30);
}
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
