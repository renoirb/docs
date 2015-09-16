---
title: length
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230738(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The length of the array.'
tags:
  - JS
  - Basic
uri: javascript/Float64Array/length

---
## Summary

The length of the array.

## Syntax

<span class="language">JavaScript</span>

    var arrayLength = float64Array.length;

## Examples

The following example shows how to get the length of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float64Array(buffer.byteLength / 8);
             alert(floatArr.length);
         }
     }
```

