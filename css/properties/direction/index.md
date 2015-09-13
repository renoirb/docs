---
title: direction
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5708516'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`ltr`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`direction`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The direction CSS property specifies the text direction/writing direction. The rtl is used for Hebrew or Arabic text, the ltr is for other languages.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/direction

---
## <span>Summary</span>

The direction CSS property specifies the text direction/writing direction. The rtl is used for Hebrew or Arabic text, the ltr is for other languages.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `ltr`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `direction`

Percentages
:   N/A

## <span>Syntax</span>

-   `direction: ltr`
-   `direction: rtl`

## <span>Values</span>

ltr
:   Default. Content flows left to right.

rtl
:   Content flows right to left.

## <span>Examples</span>

The following example demonstrates how to set and retrieve the value of the **direction** property.

``` html
<p>This is a paragraph using default writting direction(ltr).</p>

<p class="rtl">This is a paragraph using right-to-left direction.</p>

<p class="rtl" id="bidi">The paragraph using rtl and sets the bidi-override as value of unicode-bidi property.</p>
```

[View live example](http://code.webplatform.org/gist/5708516)

``` css
p {
    width: 300px;
    background-color: #cccccc;
}

.rtl {
    direction: rtl;
}

#bidi {
    unicode-bidi: bidi-override;
}
```

## <span>Notes</span>

The property does not affect alphanumeric characters in Latin documents. These characters always render **ltr**. However, the property does affect punctuation characters in Latin documents. The property pertains only to the directional flow of an element's content. It has no effect on properties such as [**left**](/css/properties/left) or [**right**](/css/properties/right), [**margin-left**](/css/properties/margin-left) or [**margin-right**](/css/properties/margin-right). The **margin-left** property, for example, sets or retrieves the width of the margin on the left side of the document regardless of the value of the **direction** property.

## <span>Related specifications</span>

[Cascading Style Sheets Level 2 Revision 1](http://www.w3.org/TR/CSS2/visuren.html#propdef-direction)
:   W3C Recommendation

## <span>See also</span>

### <span>Other articles</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `dir`
-   `Conceptual`
-   `HTML Character Sets`
