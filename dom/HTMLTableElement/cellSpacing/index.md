---
title: cellSpacing
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/HTMLTableElement
standardization_status: 'W3C Recommendation'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLTableElement/cellSpacing

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var cellSpacing = table.cellSpacing;
table.cellSpacing = newCellSpacing;
```

## Return Value

Returns an object of type NumberNumber

## Examples

This example shows how to use the **rows** collection on the [**table**](/html/elements/table) object and the **cells** collection to insert a number into each cell of the table.

``` html
<!doctype html>
<html>
 <head>
  <script>
function numberCells() {
  var count = 1;
  var oTable = document.getElementById('oTable');
  var rowsLength = oTable.rows.length;
  for (var i=0; i < rowsLength; i++) {
    var oCells = oTable.rows.item(i).cells;
    var cellsLength = oCells.length;
    for (var j=0; j < cellsLength; j++) {
      oCells.item(j).innerHTML = count++;
    }
  }
}
  </script>
 </head>
 <body onload="numberCells()">
  <table id="oTable" border="1">
<tr><th>&nbsp;</th><th>&nbsp;</th><th>&nbsp;</th><th>&nbsp;</th></tr>
<tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
<tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
  </table>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm)

## Notes

A **cells** collection is comprised of **th** and **td** objects. When a cell spans multiple rows, that cell appears only in the **cells** collection for the first of the rows that the cell spans. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position. Individual **cells** or an array of **cells** can be specified using a spreadsheet format. By specifying a colon-delimited string of the starting and ending cells, a **cells** collection can be retrieved from anywhere in the table. Specifying a particular cell with this format returns that object. The format of this string uses letters to indicate columns, starting with A, and numbers to indicate rows, starting with 1. A **cells** collection on a table row includes only the elements within that row if the *vIndex* string specifies a range of multiple rows using the spreadsheet format.

## Related specifications

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation
