---
title: margin-right
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5728056'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`Depends on the particular element. Different elements have different default margins.`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with relative lengths converted into absolute pixel values.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marginRight`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'margin-right sets the right margin of an element.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/margin-right

---
## Summary

margin-right sets the right margin of an element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `Depends on the particular element. Different elements have different default margins.`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with relative lengths converted into absolute pixel values.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `marginRight`

## Syntax

-   `margin-right: auto`
-   `margin-right: inherit`
-   `margin-right: length`
-   `margin-right: percentage`

## Values

length
:   Specifies a fixed length, using any standard [CSS length units](http://docs.webplatform.org/wiki/css/units/length) . Negative Values are allowed.

percentage
:   A percentage of the width of the containing block. Negative values are allowed. (Even though this is margin-top, the browser will take the percentage from the width, not the height of the containing block.)

auto
:   The browser calculates a right margin dependent on the space available.

inherit
:   Inherits the parent element's specified `margin-right` width.

## Examples

In this example there are three floated blocks, styled identically except for their `margin-right` values:

-   The first block has a `margin-right` of 2 centimeters, meaning that the other to blocks are pushed over to the right by 2cm. Note that a negative right margin won't make the block go outside its parent container, as is the case with a negative left margin.
-   The second block has a negative right margin — -1em — which causes the third block to be pulled over to the left, overlapping the second block slightly.
-   The third block has no `margin-right` of its own.

``` html
<div class="one"></div>
<div class="two"></div>
<div class="three"></div>
```

[View live example](http://code.webplatform.org/gist/5728056)

CSS applied to the HTML seen in the first example block.

``` css
* {
   margin: 0;
 }

 div {
   width: 200px;
   height: 100px;
   background: linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0));
   border-radius: 10px;
   float: left;
 }

 .one {
   background-color: red;
   margin-right: 2cm;
 }

 .two {
   background-color: blue;
   margin-right: -1em
 }

 .three {
   background-color: green;
 }
```

[View live example](http://code.webplatform.org/gist/5728056)

## Usage

     ===Usage===

-   When calculating the height and width of an element, DO NOT include the margins in your calculations (i.e. include everything else: content area, padding, and border). However, DO include margin size when calculating available space within an element's containing element.
-   When two margins collide, for example when one block level element has a right margin set, and a floated element directly to the right of it has a left margin set, the larger of the two margins remains, and the smaller one collapses and disappears.
-   Margins are always transparent.

### Best Practices

-   When possible, use [margin](http://docs.webplatform.org/wiki/css/properties/margin) shorthand (i.e. {margin: 10px 15px 20px 15px;}) to specify margin-widths rather than writing out each margin's specifications as this clutters code and makes it difficult to read. Use `margin-bottom` if there is a specific reason to call attention to it (e.g. one element has a different bottom margin than the rest in its class, etc.).

## Notes

### Remarks

You can specify possible length values relative to the height of the element's font (`em`) or the height of the letter "x" (`ex`). In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Microsoft Internet Explorer 4.0 and later, the margin value is absolute. The margin properties do not work with the **td** and **tr** objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 and later, apply the margin to an object, such as **div** or **p**, within the **td**. This property applies to inline elements, starting with Microsoft Internet Explorer 5.5. With earlier versions of Windows Internet Explorer, inline elements must have an **absolute** [**position**](/css/properties/position) or layout to use this property. Element layout is set by providing a value for the [**height**](/css/properties/height) property or the [**width**](/css/properties/width) property. Negative margins are supported, except for top and bottom margins on inline objects.

### Standards Information

[w3.org](http://www.w3.org/TR/CSS2/box.html#propdef-margin-right)

## Related specifications

[CSS 2](http://www.w3.org/TR/CSS2/box.html#propdef-margin-right)
:   W3C Recommendation

## See also

### Related articles

#### Box Model

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   [line-height](/css/properties/line-height)

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   **margin-right**

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `Conceptual`
-   `CSS Values and Units Reference`
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
