---
title: colorDepth
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/screen
    href: /css/cssom/screen
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/screen/colorDepth

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/screen](/css/cssom/screen)[css/cssom/screen](/css/cssom/screen)

## Syntax

``` js
var result = element.colorDepth;
element.colorDepth = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Retrieving the value of the property through script enables you to select an appropriate color to return to the client. If [**bufferDepth**](/css/cssom/screen/bufferDepth) is 0 or -1, **colorDepth** is equal to the bits-per-pixel value for the screen or printer. If **bufferDepth** is nonzero, **colorDepth** is equal to **bufferDepth**.

### Syntax

### Standards information

-   [CSSOM View Module](http://go.microsoft.com/fwlink/p/?linkid=199793), 4.2

## See also

### Related pages (MSDN)

-   `screen`
