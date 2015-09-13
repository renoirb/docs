---
title: logical and
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/719e8e30(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Performs a logical conjunction on two expressions.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/logical and'

---
## <span>Summary</span>

Performs a logical conjunction on two expressions.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result = expression1 && expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## <span>Examples</span>

``` js
console.log(true && true); // true
console.log(true && false); // false
console.log(false && true); // false
console.log(false && (3 == 4); //false
console.log("Cat" && "Dog"); //false
console.log(false && "Cat"); //false
console.log("Cat" && false); //false
```

## <span>Remarks</span>

If both expressions evaluate to true, result is true. If either expression evaluates to false, result is false.

JavaScript uses the following rules for converting non-Boolean values to Boolean values:

-   All objects are considered to be true.
-   Strings are considered to be false if they are empty.
-   null and undefined are considered to be false.
-   A Number is false if it is zero.

