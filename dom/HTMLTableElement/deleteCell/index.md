---
title: deleteCell
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLTableElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLTableElement/deleteCell

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## <span>Syntax</span>

``` js
var object = object.deleteCell(index);
```

## <span>Parameters</span>

### <span>index</span>

 Data-type
:   any

**Integer** that specifies the zero-based position of the cell to remove from the table row. If no value is provided, the last cell in the **cells** collection is deleted.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This example uses the **deleteCell** method to delete the last cell in the first row of the table.

``` html
document.all.myTable.rows[0].deleteCell()
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
