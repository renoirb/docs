---
title: getItem
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/getItem

---
## Notes

### Remarks

The returned item is the item itself and not a copy. Any changes that are made to the item are immediately reflected in the list.

### Syntax

    ISVGTransform retVal = object.getItem(index);

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.4

## See also

### Related pages (MSDN)

-   [**SVGLengthList**](/svg/objects/SVGLengthList)
-   [**SVGNumberList**](/svg/objects/SVGNumberList)
-   [**SVGPathSegList**](/svg/objects/SVGPathSegList)
-   [**SVGPointList**](/svg/objects/SVGPointList)
-   [**SVGStringList**](/svg/objects/SVGStringList)
-   [**SVGTransformList**](/svg/objects/SVGTransformList)
