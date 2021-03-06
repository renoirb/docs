---
title: terminate
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/workers/Worker
    href: /apis/workers/Worker
standardization_status: 'W3C Editor''s Draft'
summary: 'Immediately terminates the worker with which the object is associated.'
tags:
  0: API
  1: Object
  2: Methods
  4: Webworkers
uri: apis/workers/Worker/terminate

---
## Summary

Immediately terminates the worker with which the object is associated.

Method of [apis/workers/Worker](/apis/workers/Worker)[apis/workers/Worker](/apis/workers/Worker)

## Syntax

``` js
 object.terminate();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

You can terminate a worker thread inside its own code by using the **self.close()** method.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
