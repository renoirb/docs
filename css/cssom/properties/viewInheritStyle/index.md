---
title: viewInheritStyle
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/viewInheritStyle

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## <span>Syntax</span>

``` js
var result = element.viewInheritStyle;
element.viewInheritStyle = value;
```

## <span>Examples</span>

The content of the primary document is shown in the code snippet below. In the following sample a **div** tag contains a custom element that has an element behavior attached to it. The **div** tag that is located in the primary document sets a number of CSS attributes, specifically the following:

<li>
[**color**](/html/attributes/color) is set to red.

</li>
<li>
[**fontSize**](/css/properties/font-size) is set to 12 pt.

</li>
<li>
[**fontStyle**](/css/properties/font-style) is set to italic.

</li>
<li>
[**border**](/css/properties/border) is set to 2px solid blue.

</li>
``` html
<HTML xmlns:myns>
<HEAD>
<?import namespace="myns" implementation="viewInheritStyle.htc">
</HEAD>
<BODY>
<DIV style= "color:red;font-size:12pt;font-Style:italic;border:2px solid blue">
This text is inside a DIV element in the primary document.
<BR>
<!-- this is a custom element -->
<myns:abc></myns:abc>
</DIV>
</BODY>
</HTML>
```

The next code snippet shows the content of the HTC file, `viewInheritStyle.htc`.

The HTC file contains a simple document fragment, which also includes a **div** tag that uses the following CSS styles.

<li>
[**fontSize**](/css/properties/font-size) is set to 20 pt.

</li>
<li>
[**border**](/css/properties/border) is set to 2px solid green.

</li>
Because the content in the primary document has CSS styles set on a **div** tag that contains the custom element, the **div** tag in the document fragment inherits the inheritable CSS Styles when the **viewInheritStyle** property is true.

``` html
<public:component tagName="abc">
<attach event="oncontentready" onevent=init() />
</public:component>
<script>
function init(){
defaults.viewLink=document;
defaults.viewInheritStyle = false;
docFragCaption.innerText = "viewInheritStyle is now set to false";
}

function btnChangeInheritance_onClick(){
boolInherit = defaults.viewInheritStyle;

    if (boolInherit == true) {
    defaults.viewInheritStyle = false;
    docFragCaption.innerText = "viewInheritStyle is now set to false";
    }
    else
    {
    defaults.viewInheritStyle = true;
    docFragCaption.innerText = "viewInheritStyle is now set to true";
    }
}
</script>
<BODY>
<DIV id="docFragCaption" style= "font-size:20pt;border:2px solid green"></DIV>
<BR>
<INPUT id=btnChangeInheritance type=button value="Toggle viewInheritStyle property" onclick="btnChangeInheritance_onClick()">
</BODY>
```

## <span>Notes</span>

### <span>Remarks</span>

For more information on the CSS styles that can be inherited when **viewInheritStyle** is set to true, see About Viewlink CSS Inheritance. Inheritable CSS styles are only applied to elements in the document fragment that do not already have the corresponding CSS styles defined.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `defaultSelected`
-   `Conceptual`
-   `Introduction to Viewlink`
-   `About Viewlink CSS Inheritance`
-   `About Element Behaviors`
