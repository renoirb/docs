---
title: divisor
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/divisor

---
## Notes

### Remarks

After applying the [**kernelMatrix**](/svg/properties/kernelMatrix) to the input image to yield a number, that number is divided by **divisor** to yield the final destination color value. A divisor that is the sum of all the matrix values tends to have an evening effect on the overall color intensity of the result. It is an error to specify a divisor of zero. The default value is the sum of all values in **kernelMatrix**, with the exception that if the sum is zero, then the divisor is set to 1.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.25.12

## See also

### Related pages

-   [**SVGFEConvolveMatrixElement**](/svg/elements/feConvolveMatrix)
