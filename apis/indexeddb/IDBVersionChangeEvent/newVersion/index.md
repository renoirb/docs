---
title: newVersion
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBVersionChangeEvent)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBVersionChangeEvent
    href: /apis/indexeddb/IDBVersionChangeEvent
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/indexeddb/IDBVersionChangeEvent
summary: 'Returns the new version of the database, which is the version specified by the open request.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/IDBVersionChangeEvent
uri: apis/indexeddb/IDBVersionChangeEvent/newVersion

---
## Summary

Returns the new version of the database, which is the version specified by the open request.

Property of [apis/indexeddb/IDBVersionChangeEvent](/apis/indexeddb/IDBVersionChangeEvent)[apis/indexeddb/IDBVersionChangeEvent](/apis/indexeddb/IDBVersionChangeEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.newVersion;
```

## Return Value

Returns an object of type unsigned longunsigned long

A number corresponding to the value specified in the [IDBFactory.open](/apis/indexeddb/IDBFactory/open) request.

**Needs Examples**: This section should include examples.

## See also

### Related pages (MSDN)

-   `IDBVersionChangeEvent`
