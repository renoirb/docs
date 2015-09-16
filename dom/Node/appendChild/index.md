---
title: appendChild
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.appendChild](https://developer.mozilla.org/en-US/docs/Web/API/Node.appendChild) Article]'
  - 'Microsoft Developer Network: [[appendChild Method](http://msdn.microsoft.com/en-us/library/ie/ms535934(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Appends an element as a child to the object.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/appendChild

---
## Summary

Appends an element as a child to the object.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var appendedChild = node.appendChild(/* see parameter list */);
```

## Parameters

### newChild

 Data-type
:   DOM Node

 The child to append.

## Return Value

Returns an object of type DOM NodeDOM Node

The appended child.

## Examples

This example uses the **appendChild** method to add an item to an unordered list.

``` html
<!doctype html>
<script>
function fnAppend(){
   var oNewNode = document.createElement("LI");
   oList.appendChild(oNewNode);
   oNewNode.innerText="List node 5";
}
</script>
<body>
<ul id = oList>
<li>List node 1</li>
<li>List node 2</li>
<li>List node 3</li>
<li>List node 4</li>
</ul>
<input
   type = "button"
   value = "Append Child"
   onclick = "fnAppend()" />
</body>
```

## Usage

     Use this method to append elements to the end of the childNodes collection.

## Notes

To display new elements on the page, you must append them within the **body** element. For example, the following syntax demonstrates how to add a **div** element to the **body**.

    var oDiv=document.createElement("DIV");
    document.body.appendChild(oDiv);

This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render. Windows Internet Explorer 9. Exceptions are only supported when webpages are displayed in IE9 Standards mode.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
