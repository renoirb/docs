---
title: SVGPathSegCurvetoQuadraticAbs
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /svg/objects/SVGElement
standardization_status: Unknown
tags:
  - API
  - Objects
  - DOM
uri: svg/objects/SVGPathSegCurvetoQuadraticAbs

---
Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from SVGElement

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The **Q** object uses absolute coordinates to draw a quadratic Bézier curve from the current point to (x,y) by using (x1,y1) as the control point. You can specify multiple sets of coordinates to draw a polybézier. At the end of the command, the new current point becomes the final (x,y) coordinate pair that is used in the polybézier.

### Standards information

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.9

### Members

The **SVGPathSegCurvetoQuadraticAbs** object has these properties:

-   [**pathSegType**](/svg/properties/pathSegType): Gets the type of the path segment.
-   [**pathSegTypeAsLetter**](/svg/properties/pathSegTypeAsLetter): Gets the type of the path segment, specified by the corresponding one-character command name.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**x1**](/svg/properties/x1): Gets or sets the absolute or relative x-coordinate for the first control point.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
-   [**y1**](/svg/properties/y1): Gets or sets the absolute or relative y-coordinate for the first control point.
