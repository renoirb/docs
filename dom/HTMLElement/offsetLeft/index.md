---
title: offsetLeft
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetLeft.htm'
notes:
  - 'summary, clean-up of MSDN import'
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
uri: dom/HTMLElement/offsetLeft

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.offsetLeft;
element.offsetLeft = value;
```

## <span>Examples</span>

This example uses the **offsetLeft** property to determine whether an object is in the user's view.

``` html
<script type="text/javascript">
function isinView(element) {
    var oparent = element.offsetParent;
    var osleft = oID_1.offsetLeft;
    var cleft = oparent.clientWidth;
    if (osleft > cleft) {
        alert("Expand the window to see the paragraph!");
    }
}
</script>
...
<button onclick="isinView(this)">Click here</button>
...
<div id="oID_1" style="position: absolute; top:200px; left:1200px;">
...
</div>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetLeft.htm)

## <span>Notes</span>

### <span>Remarks</span>

You can determine the location, width, and height of an object by using a combination of the **offsetLeft**, [**offsetTop**](/dom/HTMLElement/offsetTop), [**offsetHeight**](/dom/HTMLElement/offsetHeight), and [**offsetWidth**](/dom/HTMLElement/offsetWidth) properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent. For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### <span>Syntax</span>