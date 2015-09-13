---
title: toPrecision
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kcs121ad(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Represents a number either in exponential or fixed-point notation with a specified number of digits.'
tags:
  0: JS
  1: Basic
  3: Function
uri: javascript/Number/toPrecision

---
## <span>Summary</span>

Represents a number either in exponential or fixed-point notation with a specified number of digits.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    toPrecision([ precision ])

**precision**
:   Optional. The number of significant digits. Must be in the range 1 - 21, inclusive.

## <span>Return Value</span>

For numbers in exponential notation, precision - 1 digits are returned after the decimal point. For numbers in fixed notation, precision significant digits are returned.

If precision is not supplied or is `undefined` , [`toString()`](/javascript/Number/toString) is called instead.

## <span>Examples</span>

Using `toPrecision` to format the decimal presentation of a number.

``` js
var pie = 3.14159;

// Call passed through to toString()
pie.toPrecision();
// Returns: "3.14159"

pie.toPrecision(5);
// Returns: "3.1416"

pie.toPrecision(2);
// Returns: "3.1"

pie.toPrecision(1);
// Returns: "3"

// Watch out for exponential notation
(1234.5).toPrecision(2);
// Returns "1.2e+3"
```

## <span>Remarks</span>

### <span>Throws</span>

[`RangeError`](/javascript/Error) when a *fractionDigits* outside the bounds of 1 - 21 (inclusive) was given.

## <span>See also</span>

### <span>Other articles</span>

-   [toExponential Method (Number)](/javascript/Number/toExponential)
-   [toFixed Method (Number)](/javascript/Number/toFixed)
-   [toString Method (Number)](/javascript/Number/toString)

### <span>External resources</span>

-   [toPrecision(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toPrecision)

### <span>Specification</span>

[15.7.4.7 Number.prototype.toPrecision(precision)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.7)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

