---
title: setCustomValidity
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLElement/setCustomValidity

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.setCustomValidity(error);
```

## Parameters

### error

 Data-type
:   any

 String containing a custom message.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The following example sets a custom message if you type "fun" into the input field.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.21.3

## See also

### Related pages

-   `HTMLObjectElement`
-   `HTMLButtonElement`
-   `HTMLFieldSetElement`
-   `HTMLInputElement`
-   `HTMLSelectElement`
-   `HTMLTextAreaElement`
