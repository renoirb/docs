---
title: canPlayType
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLMediaElement
    href: /dom/HTMLMediaElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLMediaElement
tags:
  0: API
  1: Object
  2: Methods
  4: Audio
  5: DOM
  6: Video
uri: dom/HTMLMediaElement/canPlayType

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLMediaElement](/dom/HTMLMediaElement)[dom/HTMLMediaElement](/dom/HTMLMediaElement)

## Syntax

``` js
var object = object.canPlayType();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

String

The type of media that is most likely to be rendered.

The type of media that might be able to be rendered

The media type cannot be rendered.

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.2

## See also

### Related pages

-   `media`
-   `audio`
-   `audio`
-   `video`
