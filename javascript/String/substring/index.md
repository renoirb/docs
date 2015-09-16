---
title: substring
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/3cz15ahb(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the substring at the specified location within a String object.'
tags:
  - JS
  - Basic
uri: javascript/String/substring

---
## Summary

Returns the substring at the specified location within a String object.

## Syntax

    strVariable. substring( start [, end ])

    "String Literal".substring( start [, end ] )

**start**
:   Required. The zero-based index integer indicating the beginning of the substring.

**end**
:   Optional. The zero-based index integer indicating the end of the substring. The substring includes the characters up to, but not including, the character indicated by end.If end is omitted, the characters from start through the end of the original string are returned.

## Examples

The following example illustrates the use of the **substring** method.

``` js
var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.substring(10, 15);
 document.write(ss);

 // Output:
 // brown
```

## Remarks

The substring method returns a string containing the substring from start up to, but not including, end.

The **substring** method uses the lower value of start and end as the beginning point of the substring. For example, strvar.substring(0, 3 **)** and strvar.substring(3, 0) return the same substring.

If either start or end is **NaN** or negative, it is replaced with zero.

The length of the substring is equal to the absolute value of the difference between start and end. For example, the length of the substring returned in strvar.substring(0, 3) and strvar.substring(3, 0) is three.

## See also

### Other articles

-   [substr Method (String)](/javascript/String/substr)

