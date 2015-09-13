---
title: text-overline-width
code_samples:
  - 'http://gist.github.com/7284054'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'all elements with and generated content with textual content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'see prose'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the line width for the overline text decoration.'
tags:
  - CSS
  - Properties
uri: css/properties/text-overline-width

---
## <span>Summary</span>

Specifies the line width for the overline text decoration.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   all elements with and generated content with textual content

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   see prose

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `text-overline-width: <length>`
-   `text-overline-width: <number>`
-   `text-overline-width: <percentage>`
-   `text-overline-width: auto`
-   `text-overline-width: medium`
-   `text-overline-width: normal`
-   `text-overline-width: thick`
-   `text-overline-width: thin`

## <span>Values</span>

auto
:   The user agent may use any algorithm to determine the text decoration width. The computed value is 'auto'.

normal
:   The text decoration width is the normal text decoration width for the nominal font. The computed value is 'normal'.

\<number\>
:   The text decoration width is the product of the \<number\> and the computed 'font-size'. The computed value is '\<number\>'.

\<length\>
:   The text decoration width is the length. The computed value is the corresponding absolute \<length\>.

\<percentage\>
:   The text decoration width is the product of the \<percentage\> and the computed 'font-size'. The computed value is the absolute \<length\>.

thin
:   Generates a thin line. The computed value is 'thin'.

medium
:   Generates a medium line. The computed value is 'medium'.

thick
:   Generates a thick line. The computed value is 'thick'.

## <span>Examples</span>

Example incomplete because no browser implementation exists.

``` css
p {
  text-overline-width: thick;
}
```

[View live example](http://code.webplatform.org/gist/7284054)

## <span>Related specifications</span>

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-style)
:   Candidate Recommendation
