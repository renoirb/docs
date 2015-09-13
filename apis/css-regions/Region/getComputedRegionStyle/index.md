---
title: getComputedRegionStyle()
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/css-regions/Region
    href: /apis/css-regions/Region
  return_type:
    predicate: 'Returns an object of type  '
    value: CSSStyleDeclaration
    href: /apis/css-regions/Region
standardization_status: 'W3C Working Draft'
summary: 'Returns styles calculated for an element as it appears within a region, including styles from @region rules applied to ranges within the element.'
tags:
  0: API
  1: Object
  2: Methods
  4: CSS
  5: CSS-Regions
uri: apis/css-regions/Region/getComputedRegionStyle

---
## <span>Summary</span>

Returns styles calculated for an element as it appears within a region, including styles from @region rules applied to ranges within the element.

Method of [apis/css-regions/Region](/apis/css-regions/Region)[apis/css-regions/Region](/apis/css-regions/Region)

## <span>Syntax</span>

``` js
var propValue = region.getComputedRegionStyle(element, pseudoElementName);
```

## <span>Parameters</span>

### <span>element</span>

 Data-type
:   DOM Node

 The element that contains the desired style settings, regardless of whether it currently appears within the region.

### <span>pseudoElementName</span>

 Data-type
:   String

(Optional)

The name of a CSS pseudo-element (such as **::before** or **::after**) or a null value. Optional in WebKit-based browsers.

## <span>Return Value</span>

Returns an object of type CSSStyleDeclarationCSSStyleDeclaration

Returns styles calculated for an element as it appears within a region, including styles from [**@region**](/css/atrules/@region) rules applied to ranges within the element.

## <span>Examples</span>

Check if the formatting of an element's property varies within a [region chain](/css/concepts/region_chain)

``` js
var flow = document.getNamedFlows().namedItem('sidebar');
var regions = flow.getRegions();
var contents = flow.getContent();

// get a sample of pull-quote content
var pull = contents[0].querySelector('aside.pullquote')

// are there discrepancies in how the pull-quote's text
// would be colored throughout the region chain?
varies = regionsVaryCSS(regions, pull, 'color');

function regionsVaryCSS(regs, elem, prop) {
    var values = {};
    var value, style;
    var count = 0;
    for (var i = 0; i &lt; regs.length; i++) {
        value = regs[i].getComputedRegionStyle(elem).getPropertyValue(prop);
        if (! values[value]) values[value] = 0;
        values[value]++;
    }
    for (key in values) if (values.hasOwnProperty(key)) count++;
    return count;
}
```

## <span>Usage</span>

     Behaves the same as getComputedStyle(), but incorporates CSS formatting from @region rules that may apply to individual regions.

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://www.w3.org/TR/2013/WD-css3-regions-20130528/)
:   W3C Working Draft 28 May 2013

## <span>See also</span>

### <span>Related articles</span>

#### <span>Regions</span>

-   [CSS Regions API](/apis/css-regions)

-   [CSSRegionStyleRule](/apis/css-regions/CSSRegionStyleRule)

-   [NamedFlow](/apis/css-regions/NamedFlow)

-   [firstEmptyRegionIndex](/apis/css-regions/NamedFlow/firstEmptyRegionIndex)

-   [getContent()](/apis/css-regions/NamedFlow/getContent)

-   [getRegions()](/apis/css-regions/NamedFlow/getRegions)

-   [getRegionsByContent()](/apis/css-regions/NamedFlow/getRegionsByContent)

-   [name](/apis/css-regions/NamedFlow/name)

-   [overset](/apis/css-regions/NamedFlow/overset)

-   [regionfragmentchange](/apis/css-regions/NamedFlow/regionfragmentchange)

-   [regionoversetchange](/apis/css-regions/NamedFlow/regionoversetchange)

-   [NamedFlowCollection](/apis/css-regions/NamedFlowCollection)

-   [namedItem()](/apis/css-regions/NamedFlowCollection/namedItem)

-   [Region](/apis/css-regions/Region)

-   **getComputedRegionStyle()**

-   [getRegionFlowRanges()](/apis/css-regions/Region/getRegionFlowRanges)

-   [regionOverset](/apis/css-regions/Region/regionOverset)

-   [@region](/css/atrules/@region)

-   [content fragments](/css/concepts/fragment)

-   [named flows](/css/concepts/named_flow)

-   [overset content](/css/concepts/overset)

-   [regions](/css/concepts/region)

-   [region chains](/css/concepts/region_chain)

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

### <span>External resources</span>

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
