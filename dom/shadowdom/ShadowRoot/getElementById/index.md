---
title: getElementById
notes:
  - 'Needs spec reference, usage, example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/shadowdom/ShadowRoot
    href: /dom/shadowdom/ShadowRoot
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Working Draft'
summary: 'Just like Document.getElementById except that it only works within the scope of this ShadowRoot''s shadow tree.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - Shadow
uri: dom/shadowdom/ShadowRoot/getElementById

---
## <span>Summary</span>

Just like Document.getElementById except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## <span>Syntax</span>

``` js
var result = element.getElementById();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Returns the DOM node specified by the given ID. Case matters, and if there is more than one node with the given ID, which node is returned is uncertain.

**Needs Examples**: This section should include examples.

