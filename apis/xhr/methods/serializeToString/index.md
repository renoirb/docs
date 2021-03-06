---
title: serializeToString
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/objects/XMLSerializer
    href: /apis/xhr/objects/XMLSerializer
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/xhr/objects/XMLSerializer
summary: 'Converts the parent DOM node of a document tree to an XML string.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: apis/xhr/methods/serializeToString

---
## Summary

Converts the parent DOM node of a document tree to an XML string.

Method of [apis/xhr/objects/XMLSerializer](/apis/xhr/objects/XMLSerializer)[apis/xhr/objects/XMLSerializer](/apis/xhr/objects/XMLSerializer)

## Syntax

``` js
var object = object.serializeToString(pNode);
```

## Parameters

### pNode

 Data-type
:   any

 The parent DOM node of a document tree to convert to an XML string.

## Return Value

Returns an object of type DOM NodeDOM Node

String

The string that contains an XML representation of a DOM node tree.

## Examples

To use the **serializeToString** method, type the following syntax.

``` js
oXmlSerializer =  new XMLSerializer();
sXmlString = oXmlSerializer.serializeToString(oDOMNode);
```

## See also

### Related pages

-   `XMLSerializer`
