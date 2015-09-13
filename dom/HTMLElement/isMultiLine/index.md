---
title: isMultiLine
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ismultilineEX1.htm'
notes:
  - 'summary, compatibility, rearrange MSDN content to use WPD sections'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/isMultiLine

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.isMultiLine;
element.isMultiLine = value;
```

## <span>Examples</span>

The following example shows how to use the **isMultiLine** property to determine whether the content of an object can contain only one line or multiple lines of text.

``` html
<HTML>
<HEAD>
<SCRIPT>
function answer(arg) {
    arg ? alert("Yes") : alert("No");
}
</SCRIPT>
</HEAD>
<BODY>
<P>INPUT: <INPUT type="text" ID="oInput" VALUE="oInput"/>
<BUTTON onclick="answer(oInput.isMultiLine);">
Can the INPUT contain more than one line?</BUTTON>
</P>

<P>TEXTAREA: <TEXTAREA ID="oTextarea">oTextarea</TEXTAREA>
<BUTTON onclick="answer(oTextarea.isMultiLine);">
Can the TEXTAREA contain more than one line?</BUTTON>
</P>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ismultilineEX1.htm)

### <span>Syntax</span>