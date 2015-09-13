---
title: cssText
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/css/cssText/cssText.html'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/CSSRule/CSSRule
    href: /css/cssom/CSSRule/CSSRule
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /css/cssom/CSSRule/CSSRule
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets a textual representation of a CSS rule.'
tags:
  0: API
  1: Object
  2: Properties
  4: CSS
  5: CSS-Regions
uri: css/cssom/CSSRule/cssText

---
## <span>Summary</span>

Gets or sets a textual representation of a CSS rule.

Property of [css/cssom/CSSRule/CSSRule](/css/cssom/CSSRule/CSSRule)[css/cssom/CSSRule/CSSRule](/css/cssom/CSSRule/CSSRule)

## <span>Syntax</span>

``` js
var ruleText = rule.cssText;
rule.cssText = ruleText;
```

## <span>Return Value</span>

Returns an object of type StringString

Returns a textual representation of a CSS rule.

## <span>Examples</span>

``` html
<div id="myDiv"></div>
<input type="button" value="Blue" id="blueButton">
<input type="button" value="Red" id="redButton">
<script>
    redButton.onclick=function(){
        //create a css style using cssText
        myDiv.style.cssText = "background-image: radial-gradient(red,  yellow); color: darkred;"

        // write the cssText to the contents of the div
        myDiv.innerHTML = "The cssText value is: " + myDiv.style.cssText;
    }
    blueButton.onclick=function(){
        //create a css style using cssText
        myDiv.style.cssText = "background-image: radial-gradient(blue,  white); color: darkblue;"

        // write the cssText to the contents of the div
        myDiv.innerHTML = "The cssText value is: " + myDiv.style.cssText;
    }
</script>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/css/cssText/cssText.html)

## <span>Related specifications</span>

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSSOM</span>

-   [href](/css/cssom/CSSImportRule/href)

-   [media](/css/cssom/CSSImportRule/media)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [CSSMediaList](/css/cssom/CSSMediaList/CSSMediaList)

-   [appendMedium](/css/cssom/CSSMediaList/appendMedium)

-   [deleteMedium](/css/cssom/CSSMediaList/deleteMedium)

-   [item](/css/cssom/CSSMediaList/item)

-   [mediaText](/css/cssom/CSSMediaList/mediaText)

-   [CSSMediaRule](/css/cssom/CSSMediaRule/CSSMediaRule)

-   [cssRules](/css/cssom/CSSMediaRule/cssRules)

-   [deleteRule](/css/cssom/CSSMediaRule/deleteRule)

-   [insertRule](/css/cssom/CSSMediaRule/insertRule)

-   [media](/css/cssom/CSSMediaRule/media)

-   [CSSNamespaceRule](/css/cssom/CSSNamespaceRule/CSSNamespaceRule)

-   [namespaceURI](/css/cssom/CSSNamespaceRule/namespaceURI)

-   [prefix](/css/cssom/CSSNamespaceRule/prefix)

-   [CSSOM View](/css/cssom/CSSOM_view)

-   [CSSRule](/css/cssom/CSSRule)

-   **cssText**

-   [parentStyleSheet](/css/cssom/CSSRule/parentStyleSheet)

-   [type](/css/cssom/CSSRule/type)

-   [getPropertyPriority](/css/cssom/CSSStyleDeclaration/getPropertyPriority)

-   [clipLeft](/css/cssom/properties/clipLeft)

-   [clipRight](/css/cssom/properties/clipRight)

-   [clipTop](/css/cssom/properties/clipTop)

-   [cssFloat](/css/cssom/properties/cssFloat)

-   [fontWeight](/css/cssom/properties/fontWeight)

-   [hasLayout](/css/cssom/properties/hasLayout)

-   [height](/css/cssom/properties/height)

-   [href](/css/cssom/properties/href)

-   [imports](/css/cssom/properties/imports)

-   [innerWidth](/css/cssom/properties/innerWidth)

-   [isAlternate](/css/cssom/properties/isAlternate)

-   [isPrefAlternate](/css/cssom/properties/isPrefAlternate)

-   [item](/css/cssom/properties/item)

-   [length](/css/cssom/properties/length)

-   [media](/css/cssom/properties/media)

-   [offsetX](/css/cssom/properties/offsetX)

-   [offsetY](/css/cssom/properties/offsetY)

-   [outerHeight](/css/cssom/properties/outerHeight)

-   [outerWidth](/css/cssom/properties/outerWidth)

-   [pageX](/css/cssom/properties/pageX)

-   [pageXOffset](/css/cssom/properties/pageXOffset)

-   [pageY](/css/cssom/properties/pageY)

-   [pageYOffset](/css/cssom/properties/pageYOffset)

-   [pixelBottom](/css/cssom/properties/pixelBottom)

-   [deviceXDPI](/css/cssom/screen/deviceXDPI)

-   [deviceYDPI](/css/cssom/screen/deviceYDPI)

-   [fontSmoothingEnabled](/css/cssom/screen/fontSmoothingEnabled)

-   [height](/css/cssom/screen/height)

-   [style](/css/cssom/style)

-   [type](/css/cssom/style/type)

-   [styleSheet](/css/cssom/styleSheet)

-   [addImport](/css/cssom/styleSheet/addImport)

-   [blockDirection](/css/cssom/styleSheet/blockDirection)

-   [cssRules](/css/cssom/styleSheet/cssRules)

-   [cssText](/css/cssom/styleSheet/cssText)

-   [ownerNode](/css/cssom/styleSheet/ownerNode)

-   [removeImport](/css/cssom/stylesheet/removeImport)

-   [removeRule](/css/cssom/stylesheet/removeRule)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [getComputedStyle](/dom/Window/getComputedStyle)

-   [innerHeight](/dom/Window/innerHeight)

-   [styleMedia](/dom/Window/styleMedia)
