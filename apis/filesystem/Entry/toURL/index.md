---
title: toURL
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/. example'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/Entry
    href: /apis/filesystem/Entry
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/filesystem/Entry
standardization_status: 'W3C Working Draft'
summary: "Returns a URL that can be used to identify this Entry.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/Entry/toURL

---
## Summary

Returns a URL that can be used to identify this Entry.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/Entry](/apis/filesystem/Entry)[apis/filesystem/Entry](/apis/filesystem/Entry)

## Syntax

``` js
var  = Entry.toURL();
```

## Return Value

Returns an object of type

DOMString

**Needs Examples**: This section should include examples.

## Notes

The URL has no specific expiration; as it describes a location on disk, it should be valid at least as long as that location exists.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
