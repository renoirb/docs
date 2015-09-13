---
title: getAllResponseHeaders
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns all the response headers as a string, or null if no response has been received.'
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
uri: apis/xhr/XMLHttpRequest/getAllResponseHeaders

---
## <span>Summary</span>

Returns all the response headers as a string, or null if no response has been received.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

``` js
var  = object.getAllResponseHeaders();
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

``` js
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.send();

var headers = xhr.getAllResponseHeaders().toLowerCase();
alert(headers);
```

## <span>Notes</span>

Each name/value pair in the returned string is delimited by a carriage return/line feed (CR/LF) sequence.

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
