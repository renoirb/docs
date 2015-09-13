---
title: slice
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/6w1bzf9f(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a section of a string.'
tags:
  - JS
  - Basic
uri: javascript/String/slice

---
## <span>Summary</span>

Returns a section of a string.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    stringObj.slice( start , [ end ])

**stringObj**
:   Required. A String object or string literal.

**start**
:   Required. The index to the beginning of the specified portion of stringObj.

**end**
:   Optional. The index to the end of the specified portion of stringObj. The substring includes the characters up to, but not including, the character indicated by end. If this value is not specified, the substring continues to the end of stringObj.

## <span>Examples</span>

In the first example, the slice method returns the entire string. In the second example, the slice method returns the entire string, except for the last character.

``` js
var str1 = "all good boys do fine";

 var slice1 = str1.slice(0);
 var slice2 = str1.slice(0,-1);
 var slice3 = str1.slice(4);
 var slice4 = str1.slice(4, 8);

 document.write(slice1 + "<br/>");
 document.write(slice2 + "<br/>");
 document.write(slice3 + "<br/>");
 document.write(slice4);

 // Output:
 // all good boys do fine
 // all good boys do fin
 // good boys do fine
 // good
```

## <span>Remarks</span>

The **slice** method returns a String object containing the specified portion of stringObj.

The **slice** method copies up to, but not including, the character indicated by end.

If start is negative, it is treated as length + start where length is the length of the string. If end is negative, it is treated as length + end. If end is omitted, copying continues to the end of stringObj. If end occurs before start , no characters are copied to the new string.

## <span>See also</span>

### <span>Other articles</span>

-   [slice Method (Array)](/javascript/Array/slice)

