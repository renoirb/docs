---
title: setInt8
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212461(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Stores an Int8 value at the specified byte offset from the start of the view.'
tags:
  - JS
  - Basic
uri: javascript/DataView/setInt8

---
## Summary

Stores an Int8 value at the specified byte offset from the start of the view.

## Syntax

<span class="language">JavaScript</span>

    dataView.setInt8(byteOffset, value);

**byteOffset**
:   The place in the buffer at which the value should be set.

**value**
:   The value to set.

## Examples

The following example shows how to set the first Int8 in the DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             dataView.setInt8(0, 9);
         }
     }
```

## Remarks

These methods raise an exception if they would write beyond the end of the view.

