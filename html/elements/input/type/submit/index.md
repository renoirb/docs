---
title: submit
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Merge Candidate: html/attributes/type. Add example.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'An input form button that submits the form data to the server.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
uri: html/elements/input/type/submit

---
## <span>Summary</span>

An input form button that submits the form data to the server.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Use the [**VALUE**](/html/attributes/value_(button_element)) attribute to create a button with a display label that cannot be edited by the user. The default label is `Submit Query`. If the user clicks the **Submit** button to submit the form, and that button has a [**name**](/html/attributes/name) attribute specified, that button contributes a name/value pair to the submitted data. If the **INPUT type=submit** element is part of a **FORM** element, it appears as a button with a dark border, which indicates the user can press ENTER to submit the form. When there is more than one **INPUT type=submit** in the same form, pressing enter submits the form using the first **INPUT type=submit**, unless another **INPUT type=submit** has focus. When another **INPUT type=submit** has focus, pressing enter submits the form using that **INPUT type=submit**.

### <span>Standards information</span>

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.1.19

### <span>HTML information</span>

{

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Reference`
-   `button`
-   `input`
