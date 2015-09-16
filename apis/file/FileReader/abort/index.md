---
title: abort
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[abort](https://developer.mozilla.org/en-US/docs/Web/API/FileReader.abort) Article]'
  - 'Microsoft Developer Network: [[abort Method](http://msdn.microsoft.com/en-us/library/ie/hh772297(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/FileReader
    href: /apis/file/FileReader
standardization_status: 'W3C Last Call Working Draft'
summary: 'The abort method is used to aborts the read operation. Upon return, the dom/Element/readyState will be DONE.'
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
uri: apis/file/FileReader/abort

---
## Summary

The abort method is used to aborts the read operation. Upon return, the dom/Element/readyState will be DONE.

Method of [apis/file/FileReader](/apis/file/FileReader)[apis/file/FileReader](/apis/file/FileReader)

## Syntax

``` js
 FileReader.abort();
```

## Return Value

No return value

## Examples

``` js
var instanceOfFileReader = new FileReader();

// ...read the file...
instanceOfFileReader.abort();
```

## Notes

The **abort** method is used to interrupt an asynchronous read operation that is in progress on an onloadend event, sets the state of the [dom/Element/readyState](/dom/Element/readyState) property of the FileReader to `DONE`, and sets result property to `null`.

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI/)
:   Last Call Working Draft 12 September 2013
