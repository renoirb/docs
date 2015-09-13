---
title: detail
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/CustomEvent
    href: /dom/CustomEvent
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /dom/CustomEvent
standardization_status: 'W3C Working Draft'
summary: 'Retrieves additional information about an event.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/CustomEvent/detail

---
## <span>Summary</span>

Retrieves additional information about an event.

Property of [dom/CustomEvent](/dom/CustomEvent)[dom/CustomEvent](/dom/CustomEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var eventDetails = event.detail;
```

## <span>Return Value</span>

Returns an object of type<span></span>

The content of this property is user-defined. It can be an integer, date, array, or other object type.

## <span>Examples</span>

``` js
function getCustomEventDetail(e) {
//retrieve detail for custom event
var customEventDetail = e.detail;
return customEventDetail;
}
```

## <span>Usage</span>

     Use this property to retrieve any available additional information about this developer-generated custom event. Note: It may be empty.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
