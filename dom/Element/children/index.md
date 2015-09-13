---
title: children
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/children.htm'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a live collection of child elements of an element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Element/children

---
## <span>Summary</span>

Retrieves a live collection of child elements of an element.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var childElementList = element.children;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

A live [HTMLCollection](/dom/HTMLCollection) of child elements of the element.

## <span>Examples</span>

This example shows how to retrieve a collection of **input type=text**, [**div**](/html/elements/div) and [**button**](/html/elements/button). The **children** collection for `oChildDIV` includes **p**.

``` html
<!doctype html>
<html>
 <head>
  <style>

  </style>
  <script>
/*jslint white: true, sloppy: true, plusplus: true, maxlen: 100*/
var oColl, //Collection for children.
    oRow, oCell, //Use for row and cell.
    oParentDIV, oChildDIV, oTable;
/*****************************************************************************
In:
 oColl - Collection of children.
 oCollection - Parent object.
Out:
 Output to screen.
******************************************************************************/
function getChildren(oColl, oCollection) {
  var x, length = oColl.length;
  for (x = 0; x < length; x++) {
    // Create new row.
    oRow = oTable.insertRow();

    // Create cell with the array index of current child.
    oCell = oRow.insertCell();
    oCell.align = 'center';
    oCell.style.color = '#0000FF';
    oCell.textContent = x;

    // Create cell with the tagName of current child.
    oCell = oRow.insertCell();
    oCell.align = 'center';
    oCell.textContent = oCollection.children[x].tagName;

    // Create cell with ID / name of current child.
    oCell = oRow.insertCell();
    oCell.align = 'center';

    if (oCollection.children[x].name) {
      oCell.textContent = oCollection.children[x].name;
    } else {
      oCell.textContent = oCollection.children[x].id;
    }

    // Create cell with applicable Parent object to the child.
    oCell = oRow.insertCell();
    oCell.align = 'center';
    oCell.textContent = oCollection.id;
  }
}
function collect() {
  oColl = oParentDIV.children;
  // Call function to create cells for the top parent object.
  getChildren(oColl, oParentDIV);
  /* Call function to create cells for the child within the parent object
     containing its own child.*/
  oColl = oChildDIV.children;
  getChildren(oColl, oChildDIV);
}
function b1Click() {
  collect();
  this.disabled = true;
}
function initialize() {
  oParentDIV = document.getElementById("oParentDIV");
  oChildDIV = document.getElementById("oChildDIV");
  oTable = document.getElementById("oTable");
  document.getElementById("b1").addEventListener("click", b1Click, false);
  document.getElementById("b0").addEventListener(
    "click",
    function () {
      console.log('Something.');
    },
    false);
}
window.addEventListener("load", initialize, false);
  </script>
 </head>
 <body>
  <center>
   <span class="oTitle">DIV Object (ID: oParentDIV)</span>
   <div id="oParentDIV" class="oDIV">
    Some Input (non-editable):
    <input type="text" name="SomeInputTextBox"
      value="" size="5" contenteditable="false"/>
    <div id="oChildDIV">
     <p id="oParagraph1">Some text in a paragraph</p>
    </div>
    <button id="b0" name="SomeButton">The Label for the Button</button>
   </div>
   <hr/>
   <button id="b1" style="cursor: pointer;">Retrieve Collection</button>
   <br/><br/>
   <table border="1" id="oTable" alt="Child Listing">
    <tr>
     <th>Array Index</th>
     <th>Child Element</th>
     <th>ID</th>
     <th>Parent Object</th>
    </tr>
   </table>
  </center>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/children.htm)

## <span>Usage</span>

     Use this property to get a live collection of the child elements of an element.

## <span>Notes</span>

-   Since this is a live collection, its **length**, as well as its content, will always change whenever child elements are added, removed, or reordered.
-   The objects contained in the **children** collection are undefined if the child elements are overlapping tags.
-   The **children** collection can contain HTML elements.

## <span>Related specifications</span>

[WHATWG DOM](http://dom.spec.whatwg.org/)
:   Living Standard

[DOM4](http://www.w3.org/TR/dom/)
:   Working Draft
