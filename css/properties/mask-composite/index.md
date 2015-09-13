---
title: mask-composite
notes:
  - 'As of time of writing, this property is not yet implemented in most browsers.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`add`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'no'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property allows to composite multiple mask layers define by mask-image with different Porter-Duff compositing modes. As of time of writing, this property is not yet implemented in most browsers.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-composite

---
## <span>Summary</span>

This property allows to composite multiple mask layers define by mask-image with different Porter-Duff compositing modes. As of time of writing, this property is not yet implemented in most browsers.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `add`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   no

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `mask-composite: add`
-   `mask-composite: exclude`
-   `mask-composite: intersect`
-   `mask-composite: subtract`

## <span>Values</span>

add
:   The mask image layer closer to the user is placed above the next mask image layer.

subtract
:   The mask image layer closer to the user is placed where it falls outside of the next mask image layer.

intersect
:   The parts of the mask image layer closer to the user that overlap the next mask image layer replace the parts of the next mask image layer.

exclude
:   The non-overlaping parts of the mask image layer closer to the user and the next mask image layer are combined.

## <span>Examples</span>

``` css
/* The two mask layers are composited with the operation 'exclude' */
mask-image: url(source.png), url(destination.png);
mask-composite: exclude;
```

``` css
/* destination.png and background.png are combined
with the compositing operator subtract.
The result of this operation and source.png are combined
with the compositing operator exclude. */
mask-image: url(source.png), url(destination.png), url(background.png);
mask-composite: exclude, subtract;
```

``` css
/* Just one mask layer is specified. No compositing operation will happen. */
mask-image: url(source.png);
mask-composite: exclude;
```

## <span>Usage</span>

     Safari, Chrome and Opera implement this property '-webkit-' prefixed with different keywords. The keywords can be mapped as follows:

add → source-over, subtract → source-out, intersect → source-in, exclude → xor

## <span>Related specifications</span>

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor's Draft
