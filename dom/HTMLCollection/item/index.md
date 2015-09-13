---
title: item
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLCollection
    href: /dom/HTMLCollection
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLCollection
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).'
tags:
  - API
  - Object
  - Methods
  - DOM
  - HTML
  - JavaScript
uri: dom/HTMLCollection/item

---
## <span>Summary</span>

Retrieves a node specified by ordinal index. Nodes are numbered in tree order (depth-first traversal order).

Method of [dom/HTMLCollection](/dom/HTMLCollection)[dom/HTMLCollection](/dom/HTMLCollection)

## <span>Syntax</span>

``` js
var node = collection.item(index);
```

## <span>Parameters</span>

### <span>index</span>

 Data-type
:   unsigned long

 The index of the node to be fetched. The index origin is 0.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The **Node** at the corresponding position upon success. A value of **null** is returned if the index is out of range.

**Needs Examples**: This section should include examples.

