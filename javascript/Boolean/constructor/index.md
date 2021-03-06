---
title: constructor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155289(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Initializes a Boolean object.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Boolean/constructor

---
## Summary

Initializes a Boolean object.

## Syntax

    boolean.constructor([ value ])

**boolean**
:   Required. The name of the Boolean object being created

**value**
:   Optional. Specifies the value of the Boolean object. This can be the numbers 1 or 0, or the strings "true" or "false".

## Examples

The following example illustrates the use of the constructor property.

``` js
var x = new Boolean("true");
 if (x.constructor == Boolean)
     document.write("Object is a Boolelan.");

 // Output:
 // Object is a Boolean.
```

## Remarks

The **constructor** property contains a reference to the function that constructs instances of the Boolean object.

## See also

### Specification

[15.6 Boolean Objects](http://www.ecma-international.org/ecma-262/5.1/#sec-15.6) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

