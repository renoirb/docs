---
title: namedItem
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN content'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLElement/namedItem

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var object = object.namedItem(name);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   BSTR

 A **String** that specifies the [**name**](/html/attributes/name) or [**id**](/html/attributes/id) property of the object to retrieve. A collection is returned if more than one match is made.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Object

## <span>Examples</span>

The following example shows how to use the **namedItem** method to retrieve a **div** and change its [**innerText**](/dom/HTMLElement/innerText) property.

``` html
<div id="oDIV1">This text will not change.</div>
<div id="oDIV2">This text will change.</div>
<button onclick="document.all.namedItem('oDIV2').innerHTML='Changed!';">
   Change Option
</button>
```

## <span>Notes</span>

### <span>Remarks</span>

Windows Internet Explorer 8 and later. In IE8 Standards mode, the **namedItem** method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched Defining Document Compatibility. The **namedItem** method was introduced in Microsoft Internet Explorer 6. The **namedItem** method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched **element**. This method first searches for an object with a matching [**id**](/html/attributes/id) attribute. If a match is not found, the method searches for an object with a matching [**name**](/html/attributes/name) attribute, but only on those elements that are allowed a name attribute.

### <span>Standards information</span>

There are no standards that apply here.