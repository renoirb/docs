---
title: insertAdjacentHTML
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertscript_1.htm'
notes:
  - 'Needs compat'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
standardization_status: Mixed
summary: 'Parses and inserts HTML code at or beyond the edges of an element within the document hierarchy.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/insertAdjacentHTML

---
## <span>Summary</span>

Parses and inserts HTML code at or beyond the edges of an element within the document hierarchy.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
 element.insertAdjacentHTML(where, html);
```

## <span>Parameters</span>

### <span>where</span>

 Data-type
:   String

 Where to insert the HTML text. Must be one of the following values:

|Value|Description|
|:----|:----------|
|"beforebegin"|Before the element itself.|
|"afterbegin"|Just inside the element, before its first child.|
|"beforeend"|Just inside the element, after its last child.|
|"afterend"|After the element itself.|

### <span>html</span>

 Data-type
:   String

 Well-formed HTML code to insert. The string can be a combination of text and HTML tags.

## <span>Return Value</span>

No return value

## <span>Examples</span>

This example uses the **insertAdjacentHTML** method to insert script into the page.

``` js
var sHTML="<input type=button onclick=" +
    "go2()" + " value='Click Me'><BR>"
var sScript='<SCRIPT DEFER>'
sScript = sScript +
    'function go2(){ alert("Hello from inserted script.") }'
sScript = sScript + '</script' + '>';
ScriptDiv.insertAdjacentHTML("afterBegin",sHTML + sScript);
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertscript_1.htm)

## <span>Usage</span>

     Use this method to add HTML to the page before/after an element or at the beginning or at the end of an element.

## <span>Notes</span>

-   In XML documents, this methods will fail if the **html** parameter is not well-formed, valid HTML.
-   This method will fail if "afterend" or "beforebegin" is used when the context is the root element of the document.
-   If the text contains HTML tags, the method parses and formats the text as it is inserted.

**TODO**: The notes below need to be verified.

-   You cannot insert text while the document is loading. Wait for the [**onload**](/dom/Element/load) event to fire before attempting to call this method.
-   When using the **insertAdjacentHTML** method to insert script, you must include the [**DEFER**](/html/attributes/defer) attribute in the [**script**](/html/elements/script) element.

## <span>Related specifications</span>

[DOM Parsing and Serialization](http://domparsing.spec.whatwg.org/)
:   Living Standard

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `innerHTML`
-   `outerHTML`
