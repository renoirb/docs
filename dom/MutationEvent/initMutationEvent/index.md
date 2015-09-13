---
title: initMutationEvent
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Mutation Events](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Mutation_events) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/MutationEvent
    href: /dom/MutationEvent
standardization_status: Deprecated
summary: 'Initializes a new DOM mutation (modification) event that the createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
uri: dom/MutationEvent/initMutationEvent

---
## <span>Summary</span>

Initializes a new DOM mutation (modification) event that the createEvent method created.

Method of [dom/MutationEvent](/dom/MutationEvent)[dom/MutationEvent](/dom/MutationEvent)

## <span>Syntax</span>

``` js
 event.initMutationEvent(/* see parameter list */);
```

## <span>Parameters</span>

### <span>eventType</span>

 Data-type
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### <span>canBubble</span>

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### <span>cancelable</span>

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### <span>relatedNode</span>

 Data-type
:   DOM Node

 A secondary node that is related to the event. Sets the value for the [**relatedNode**](/dom/MutationEvent/relatedNode) property.

### <span>prevValue</span>

 Data-type
:   String

 The previous value of the attribute or text node. Sets the value for the [**prevValue**](/dom/MutationEvent/prevValue) property.

### <span>newValue</span>

 Data-type
:   String

 The new value of the attribute or text node. Sets the value for the [**newValue**](/dom/MutationEvent/newValue) property.

### <span>attrName</span>

 Data-type
:   String

 The name of the changed attribute in a **DOMAttrModified** event. Sets the value for the [**attrName**](/dom/MutationEvent/attrName) property.

### <span>attrChange</span>

 Data-type
:   String

 The type of modification in a **DOMAttrModified** event. Sets the value for the [**attrChange**](/dom/MutationEvent/attrChange) property.

## <span>Return Value</span>

No return value

## <span>Related specifications</span>

[DOM Level 2 Events](http://www.w3.org/TR/DOM-Level-2-Events/)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Deprecated</span>

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   **initMutationEvent**

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)
