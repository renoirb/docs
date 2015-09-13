---
title: getAttributeNodeNS
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example and compat tables'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Gets an attribute node that matches the specified namespace and name.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/getAttributeNodeNS

---
## <span>Summary</span>

Gets an attribute node that matches the specified namespace and name.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var attributeNode = element.getAttributeNodeNS(namespace, name);
```

## <span>Parameters</span>

### <span>namespace</span>

 Data-type
:   String

 The namespace URI that defines the desired attribute, or a null value.

### <span>name</span>

 Data-type
:   Blob

 The name of the desired attribute, or a null value.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

An attribute node that matches the specified namespace and attribute name, or a null value when no attribute node is found.

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
