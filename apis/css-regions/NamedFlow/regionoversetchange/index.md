---
title: regionoversetchange
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Fires on the NamedFlow object when a change in how its content flows through a region chain renders any region empty or overset (overfilled), or that reverses that state.'
tags:
  - Events
  - API
  - CSS
  - CSS-Regions
uri: apis/css-regions/NamedFlow/regionoversetchange

---
## <span>Summary</span>

Fires on the NamedFlow object when a change in how its content flows through a region chain renders any region empty or overset (overfilled), or that reverses that state.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
[**NamedFlow**](/apis/css-regions/NamedFlow)

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
none

</td>
</tr>
</table>
Fires on the [**NamedFlow**](/apis/css-regions/NamedFlow) object when the tail end of content moves from one region to another within a [chain](/css/concepts/region_chain), changing any between a properly filled state and one that is empty or [*overset*](/css/concepts/overset).

## <span>Examples</span>

dispatch functions to add or delete regions based on changes to how content flows through a region chain:

``` js
document.getNamedFlows().namedItem('main').addEventListener(
    'regionoversetchange', modifyFlow
);

function modifyFlow(e) {
    var flow = e.target;
    if (flow.overset) {
        appendRegion(flow.name); // custom function
    }
    else if (flow.firstEmptyRegionIndex !== -1) {
        trimRegions(flow.name); // custom function
    }
}
```

## <span>Notes</span>

The event fires when the [**regionOverset**](/apis/css-regions/Region/regionOverset) changes (between **fit**, **overset**, and **empty**) for any region within a [region chain](/css/concepts/region_chain). (Compare with the [**regionfragmentchange**](/apis/css-regions/NamedFlow/regionfragmentchange) event, which fires much more frequently in response to changing content or dimensions.)

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

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

-   **regionoversetchange**

-   [NamedFlowCollection](/apis/css-regions/NamedFlowCollection)

-   [namedItem()](/apis/css-regions/NamedFlowCollection/namedItem)

-   [Region](/apis/css-regions/Region)

-   [getComputedRegionStyle()](/apis/css-regions/Region/getComputedRegionStyle)

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
