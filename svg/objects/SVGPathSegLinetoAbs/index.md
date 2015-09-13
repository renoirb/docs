---
title: SVGPathSegLinetoAbs
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
uri: svg/objects/SVGPathSegLinetoAbs

---
Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Inherited from SVGElement</span>

### <span>Properties</span>

*No properties.*

### <span>Methods</span>

*No methods.*

### <span>Events</span>

*No events.*

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The **L** object uses absolute coordinates to draw a line from the current point to the given (x,y) coordinate, which becomes the new current point. You can specify a number of coordinates pairs to draw a polyline. At the end of the command, the new current point is set to the final set of coordinates that are provided.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.5

### <span>Members</span>

The **SVGPathSegLinetoAbs** object has these properties:

-   [**pathSegType**](/svg/properties/pathSegType): Gets the type of the path segment.
-   [**pathSegTypeAsLetter**](/svg/properties/pathSegTypeAsLetter): Gets the type of the path segment, specified by the corresponding one-character command name.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
