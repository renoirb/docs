---
title: filesystem
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/filesystem/Entry
    href: /apis/filesystem/Entry
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/filesystem/Entry
standardization_status: 'W3C Working Draft'
summary: "The file system on which the Entry resides.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: FileSystemAPI
uri: apis/filesystem/Entry/filesystem

---
## Summary

The file system on which the Entry resides.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Property of [apis/filesystem/Entry](/apis/filesystem/Entry)[apis/filesystem/Entry](/apis/filesystem/Entry)

## Syntax

**Note**: This property is read-only.

``` js
var result = Entry.filesystem;
```

## Return Value

Returns an object of type

FileSystem

**Needs Examples**: This section should include examples.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
