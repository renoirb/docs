---
title: removeAttribute
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Removes a specified content attribute from an element.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/removeAttribute

---
## Summary

Removes a specified content attribute from an element.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
 element.removeAttribute(name);
```

## Parameters

### name

 Data-type
:   String

 The name of the attribute.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Use this method to remove a content attribute from an element.

## Notes

-   The attribute to remove may not exist in the first place.

## Related specifications

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[Document Object Model (DOM) Level 1](http://www.w3.org/TR/REC-DOM-Level-1)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard

## See also

### Related pages (MSDN)

-   `getAttribute`
-   `setAttribute`
