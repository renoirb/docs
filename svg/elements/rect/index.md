---
title: rect
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/44786e14924371effbe4'
  - 'http://gist.github.com/9697f0fe090f4ad2e6e9'
notes:
  - 'Fix multiple broken links'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGRectElement](/dom/SVGRectElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The rect element is a SVG basic shape to create a rectangle starting with a given with and height beginning at a x- and y-point.'
tags:
  - Markup
  - Elements
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/attributes/style
    - svg/attributes/class
    - svg/attributes/externalResourcesRequired
    - svg/attributes/transform
    - svg/attributes/x
    - svg/attributes/y
    - svg/attributes/width
    - svg/attributes/height
    - svg/attributes/rx
    - svg/attributes/ry
uri: svg/elements/rect

---
## Summary

The rect element is a SVG basic shape to create a rectangle starting with a given with and height beginning at a x- and y-point.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGRectElement](/dom/SVGRectElement)

## Examples

In the following code example, the rect element is used to draw a purple rectangle.

``` html


<svg width="200" height="200" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="5" width="100" height="80" fill="purple" />
</svg>
```

</pre>
[View live example](http://code.webplatform.org/gist/44786e14924371effbe4)

In the following code example, the rect element is used to create a orange rectangle with rounded corners.

``` html


<svg width="200" height="200" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="5" width="100" height="80" fill="orange" rx="10" ry="10" />
</svg>
```

</pre>
[View live example](http://code.webplatform.org/gist/9697f0fe090f4ad2e6e9)

### Attributes

#### Global attributes

-   [**Conditional processing attributes**](/svg/attributes#Conditional_Processing_Attributes)
-   [**Core attributes**](/svg/attributes#Core_Attributes)
-   [**Graphical events attributes**](/svg/attributes#Graphical_Event_Attributes)
-   [**Presentation attributes**](/svg/attributes#Presentation_Attributes)

-   [**style**](/w/index.php?title=svg/attributes/style&action=edit&redlink=1)
-   [**class**](/w/index.php?title=svg/attributes/class&action=edit&redlink=1)
-   [**externalResourcesRequired**](/w/index.php?title=svg/attributes/externalResourcesRequired&action=edit&redlink=1)
-   [**transform**](/w/index.php?title=svg/attributes/transform&action=edit&redlink=1)

#### Specific attributes

-   [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1)
-   [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1)
-   [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1)
-   [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1)
-   [**rx**](/w/index.php?title=svg/attributes/rx&action=edit&redlink=1)
-   [**ry**](/w/index.php?title=svg/attributes/ry&action=edit&redlink=1)

### DOM Interface

This element implements the [**SVGRectElement**](/dom/SVGRectElement) interface.

### Members

The **SVGRectElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGRectElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGRectElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**pointerEvents**](/svg/attributes/pointers): Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**rx**](/svg/properties/rx_(SVGRectElement)): Gets or sets the x-axis radius of a rounded corner rectangle.
-   [**ry**](/svg/properties/ry_(SVGRectElement)): Gets or sets the y-axis radius of a rounded corner rectangle.
-   [**stroke**](/svg/attributes/stroke): Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
-   [**strokeDasharray**](/svg/attributes/stroke-dasharray): Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
-   [**strokeDashoffset**](/svg/attributes/stroke-dashoffset): Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
-   [**strokeLinecap**](/svg/attributes/stroke-linecap): Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
-   [**strokeLinejoin**](/svg/attributes/stroke-linejoin): Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
-   [**strokeMiterlimit**](/svg/attributes/stroke-miterlimit): Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [**strokeLinejoin**](/svg/attributes/stroke-linejoin) property).
-   [**strokeOpacity**](/svg/attributes/stroke-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
-   [**strokeWidth**](/svg/attributes/stroke-width): Sets or retrieves a value that specifies the width of the stroke on the current object.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Related specifications

[The ‘rect’ element](http://www.w3.org/TR/SVG11/shapes.html#RectElement)
:   W3C Recommendation
