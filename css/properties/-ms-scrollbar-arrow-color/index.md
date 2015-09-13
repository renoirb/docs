---
title: -ms-scrollbar-arrow-color
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarColor.htm'
notes:
  - 'Add summery, values, specifications, compatibility.'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/properties
    href: /css/properties
standardization_status: Non-Standard
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/properties/-ms-scrollbar-arrow-color

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/properties](/css/properties)[css/properties](/css/properties)

## <span>Syntax</span>

``` js
var result = element.-ms-scrollbar-arrow-color;
element.-ms-scrollbar-arrow-color = value;
```

## <span>Examples</span>

The following example shows how to create a style rule that sets the **-ms-scrollbar-arrow-color** property for a **textArea** element.

``` html
<HTML>
  <HEAD>
    <STYLE>
        TEXTAREA.BlueArrow  { scrollbar-arrow-color:blue }
    </STYLE>
  </HEAD>
  <BODY>
    <TEXTAREA CLASS="BlueArrow">The arrows in the scroll bar for
    this element will be blue.</TEXTAREA>
  </BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarColor.htm)

## <span>Notes</span>

### <span>Remarks</span>

Windows Internet Explorer 8. The **-ms-scrollbar-arrow-color** attribute is an extension to CSS, and can be used as a synonym for **scrollbar-arrow-color** in IE8 Standards mode. The scroll arrows, located at each end of a scroll bar, are the square buttons containing the arrows that move the content on the screen in small increments, either up and down or left and right. This property applies to elements that display a scroll bar. Cascading Style Sheets (CSS) enable scrolling on all objects through the [**overflow**](/css/properties/overflow) property. These objects are not listed in the Applies To list for this property.

### <span>Syntax</span>

`-ms-scrollbar-arrow-color: variant`

### <span>Standards information</span>

There are no standards that apply here.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Scrollbar</span>

-   [-ms-scrollbar-3d-light-color](/css/properties/-ms-scrollbar-3d-light-color)

-   **-ms-scrollbar-arrow-color**

-   [-ms-scrollbar-base-color](/css/properties/-ms-scrollbar-base-color)

-   [-ms-scrollbar-darkshadow-color](/css/properties/-ms-scrollbar-darkshadow-color)

-   [-ms-scrollbar-face-color](/css/properties/-ms-scrollbar-face-color)

-   [-ms-scrollbar-highlight-color](/css/properties/-ms-scrollbar-highlight-color)

-   [-ms-scrollbar-shadow-color](/css/properties/-ms-scrollbar-shadow-color)

-   [-ms-scrollbar-track-color](/css/properties/-ms-scrollbar-track-color)

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaultSelected`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `-ms-scrollbar-3dlight-color`
-   `-ms-scrollbar-base-color`
-   `-ms-scrollbar-darkshadow-color`
-   `-ms-scrollbar-face-color`
-   `-ms-scrollbar-highlight-color`
-   `-ms-scrollbar-shadow-color`
-   `-ms-scrollbar-track-color`
