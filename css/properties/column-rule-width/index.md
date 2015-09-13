---
title: column-rule-width
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6288958'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`medium`'
  'Applies to': 'multi-column elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'absolute length; ‘0’ if the column rule style is ‘none’ or ‘hidden’'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnRuleWidth`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the width of the rule between columns.'
tags:
  - CSS
  - Properties
uri: css/properties/column-rule-width

---
## <span>Summary</span>

Specifies the width of the rule between columns.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `medium`

Applies to
:   multi-column elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   absolute length; ‘0’ if the column rule style is ‘none’ or ‘hidden’

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `columnRuleWidth`

Percentages
:   N/A

## <span>Syntax</span>

-   `column-rule-width: 0`
-   `column-rule-width: medium`
-   `column-rule-width: thick`
-   `column-rule-width: thin`
-   `column-rule-width: width`

## <span>Values</span>

medium
:   Default. A medium width border.

thin
:   Width less than the default.

thick
:   Width greater than the default.

width
:   Width consisting of a floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`)

0
:   If the column rule style is ‘none’ or ‘hidden’

## <span>Examples</span>

Makes 3 columns with 4px dashed green column-rule.

``` css
/*
Makes 3 columns with 4px dashed green column-rule
*/

#columns {
  columns: 3;

  /* Prefix free example below, use vendor prefixes where needed */
  column-rule-style: dashed;
  column-rule-color: green;
  column-rule-width: 5px;
}
```

[View live example](http://code.webplatform.org/gist/6288958)

## <span>Usage</span>

     * Negative length values are not allowed.

## <span>Notes</span>

The exact thickness of the column rule when using the `medium`, `thin`, or `thick` value is user agent dependent, and is not defined in the specification.

## <span>Related specifications</span>

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   W3C Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Multi-Column</span>

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   **column-rule-width**

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)
