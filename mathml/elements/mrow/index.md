---
title: mrow
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mrow)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mrow element is used to group sub-expressions, which usually contain one or more operators with their respective operands (such as mi and mn). This element renders as a horizontal row containing its arguments.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mrow

---
## <span>Summary</span>

The MathML mrow element is used to group sub-expressions, which usually contain one or more operators with their respective operands (such as mi and mn). This element renders as a horizontal row containing its arguments.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## <span>Examples</span>

This example demonstrates a simple usage of the mrow element:

``` html


<math>

  <mrow>
    <mn> 1 </mn>
    <mo> + </mo>
    <mn> 1 </mn>
  </mrow>

  <mrow>
    <mo> ( </mo>
    <mrow>
      <mi> x </mi>
      <mo> , </mo>
      <mi> y </mi>
    </mrow>
    <mo> ) </mo>
  </mrow>

</math>
```

</pre>

## <span>Related specifications</span>

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mrow)
:   W3C Recommendation

When writing a MathML expression, you should group elements within an \<mrow\> in the same way as they are grouped in the mathematical interpretation of the expression. Proper grouping helps the rendering of the expression in several ways:

-   It can improve the display by possibly affecting spacing.
-   It allows for more intelligent line-breaking and indentation.
-   It simplifies the interpretation of the expression by automated systems such as computer algebra systems and audio renderers.
