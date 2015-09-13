---
title: user-select
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://jsfiddle.net/R5Ygm/'
notes:
  - "Editing this page produces: \"Warning: More than one default form is defined for this page.\"\_?"
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`all`'
  'Applies to': 'Visible elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Controls the visible highlighting of selections of text and elements. It is possible to blind out selection completely or to allow the selection of text only.'
tags:
  0: CSS
  1: Properties
  3: Design
  5: Selectors
uri: css/properties/user-select

---
## <span>Summary</span>

Controls the visible highlighting of selections of text and elements. It is possible to blind out selection completely or to allow the selection of text only.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `all`

Applies to
:   Visible elements

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

## <span>Syntax</span>

-   `user-select: all`
-   `user-select: element`
-   `user-select: none`
-   `user-select: text`

## <span>Values</span>

none
:   None of the descendants of the element can be selected, neither text nor images.

text
:   Only text of the element and its descendants can be selected.

all
:   Default. Everything, text and images, can be selected.

element
:   Only specified elements can be selected. Only supported in Firefox and Internet Explorer.

## <span>Examples</span>

Deactivate selection of text for elements with the class **no-select**.

``` css
.no-select {
    user-select: none;
}
```

[View live example](http://jsfiddle.net/R5Ygm/)

## <span>Usage</span>

     Needs vendor prefixes.

## <span>Notes</span>

Also works on mobile devices to suppress selection by touch and hold.

## <span>Related specifications</span>

[User Interface for CSS3](http://www.w3.org/TR/2000/WD-css3-userint-20000216)
:   W3C Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Attributes</span>

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   **user-select**

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages (MSDN)</span>

-   `IE Test Drive: User-Select`
-   `[1]`
