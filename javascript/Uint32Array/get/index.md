---
title: get
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
readiness: 'Ready to Use'
summary: 'Omittable. Gets the element at the specified index.'
tags:
  - JS
  - Basic
uri: javascript/Uint32Array/get

---
## Summary

Omittable. Gets the element at the specified index.

## Syntax

    var value = uint32Array.get(index);

**value**
:   The value returned by this method.

**index**
:   The index at which to get the element of the array.

## Examples

The following example shows how to get the first element of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int32Array(buffer.byteLength / 4);
             var element = intArr.get(0);
         }
     }
```

