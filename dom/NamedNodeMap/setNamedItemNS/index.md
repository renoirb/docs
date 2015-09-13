---
title: setNamedItemNS
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]'
  - 'Microsoft Developer Network: [[setNamedItemNS Method](http://msdn.microsoft.com/en-us/library/ie/ff975204(v=vs.85).aspx) Article]'
notes:
  - 'example required'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/NamedNodeMap
    href: /dom/NamedNodeMap
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/NamedNodeMap
standardization_status: 'W3C Recommendation'
summary: 'Sets an attribute object as part of the object.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/NamedNodeMap/setNamedItemNS

---
## <span>Summary</span>

Sets an attribute object as part of the object.

Method of [dom/NamedNodeMap](/dom/NamedNodeMap)[dom/NamedNodeMap](/dom/NamedNodeMap)

## <span>Syntax</span>

``` js
var object = object.setNamedItemNS(/* see parameter list */);
```

## <span>Parameters</span>

### <span>pAttrNode</span>

 Data-type
:   any

 The [**attribute**](/dom/HTMLElement) to add.

### <span>ppNodeOut</span>

 Data-type
:   any

 The [**attribute**](/dom/HTMLElement) node that the *pAttrNode* node replaces, or a null value.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

{

**Needs Examples**: This section should include examples.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4
