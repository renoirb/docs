---
title: setEnd
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.setEnd](https://developer.mozilla.org/en-US/docs/Web/API/Range.setEnd) Article]'
  - 'Microsoft Developer Network: [[setEnd Method](http://msdn.microsoft.com/en-us/library/ie/ff975448(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Sets the end point of the range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/setEnd

---
## <span>Summary</span>

Sets the end point of the range.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## <span>Syntax</span>

``` js
var result = range.setEnd(/* see parameter list */);
```

## <span>Parameters</span>

### <span>endNode</span>

 Data-type
:   DOM Node

 A node in the document hierarchy.

### <span>offset</span>

 Data-type
:   Number

 Specifies the offset value for the end point.

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|InvalidStateError|detach has been invoked on the object.|
|W3Exception\_DOM\_INDEX\_SIZE\_ERR|offset is negative or greater than the number of child units in refNode.|

## <span>Examples</span>

``` js
var range = document.createRange();
var endNode = document.getElementsByTagName("p").item(3);
var endOffset = document.getElementsByTagName("p").item(3).childNodes.length;
range.setEnd(endNode,endOffset);
```

### <span>Syntax</span>

range.setEnd(endNode, endOffset);

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## <span>Related specifications</span>

[DOM](http://dom.spec.whatwg.org/#dom-range-setend)
:   Living Standard
