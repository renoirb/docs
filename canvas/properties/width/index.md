---
title: width
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "\nMove Candidate:   Probably should be under HTML5 canvas element. See HTML5 specification.\n\n"
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLCanvasElement
    href: /dom/HTMLCanvasElement
summary: 'Width property of canvas element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: canvas/properties/width

---
## <span>Summary</span>

Width property of canvas element.

Property of [dom/HTMLCanvasElement](/dom/HTMLCanvasElement)[dom/HTMLCanvasElement](/dom/HTMLCanvasElement)

## <span>Syntax</span>

``` js
var result = element.width;
element.width = value;
```

## <span>Examples</span>

The following code example uses the **width** and [**height**](/canvas/properties/height_(canvas)) property to get and set the attributes of a [**canvas**](/canvas/objects/canvas) element on the document.

``` html
<!DOCTYPE html>
<head>
  <script type="text/javascript">
function draw()
{
  var canvas = document.getElementById("MyCanvas");
  if (canvas.getContext)
    {
    var ctx = canvas.getContext("2d");
    ctx.fillStyle = "blue";
    ctx.fillRect(0,0,canvas.width,canvas.height);
    }
}
function change(val)
    {
    var canvas = document.getElementById("MyCanvas");
    canvas.width = canvas.width + val;
    canvas.height = canvas.height + val;
    draw();
    }
  </script>
</head>
<body onload="draw()" bgcolor="lightgray" >
      <div>
      <button onclick="change(10)">Make canvas larger</button>
      <button onclick="change(-10)">Make canvas smaller</button>
      </div>
      <div>
        <canvas id="MyCanvas" width="500" height="500" > </canvas>
      </div>
  </body>
</html>
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.10

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `canvas`
