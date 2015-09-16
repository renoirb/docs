---
title: layout-grid
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add summery, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`both loose none none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
tags:
  - CSS
  - Properties
uri: css/properties/layout-grid

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `both loose none none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `layout-grid: char`
-   `layout-grid: line`
-   `layout-grid: mode`
-   `layout-grid: type`

## Values

mode
:   Any of the range of mode values available to the [**-ms-layout-grid-mode**](/css/properties/layout-grid-mode) property.

type
:   Any of the range of type values available to the [**-ms-layout-grid-type**](/css/properties/layout-grid-type) property.

line
:   Any of the range of line values available to the [**-ms-layout-grid-line**](/css/properties/layout-grid-line) property.

char
:   Any of the range of character values available to the [**-ms-layout-grid-char**](/css/properties/layout-grid-char) property.

## Examples

This example uses the **-ms-layout-grid** attribute to specify character layout for a block of text.

``` html
<STYLE>
DIV.layout { layout-grid: both fixed 12px 12px }
</STYLE>
<DIV CLASS = "layout">
This is a block element containing a sentence of sample text.
</DIV>
```

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-layout-grid** attribute is an extension to CSS, and can be used as a synonym for **layout-grid** in IE8 Standards mode. Though you don't have to specify all four values for the **-ms-layout-grid** attribute, they must be listed in the order given in Possible Values. Web documents in Asian languages, such as Chinese or Japanese, usually create a page layout for characters using a one-dimensional or two-dimensional grid. You can use the **-ms-layout-grid** attribute to incorporate this layout into Web documents.

### Syntax

`-ms-layout-grid: mode type line char`

### Standards information

There are no standards that apply here.

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   **layout-grid**

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaultSelected`
-   `runtimeStyle`
-   `style`
