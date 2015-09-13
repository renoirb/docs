---
title: data
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'example, standards, compatibility'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MessageEvent
    href: /dom/MessageEvent
  return:
    predicate: 'Returns an object of type '
    value: any
    href: /dom/MessageEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the content of the message.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/MessageEvent/data

---
## <span>Summary</span>

Gets the content of the message.

Property of [dom/MessageEvent](/dom/MessageEvent)[dom/MessageEvent](/dom/MessageEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var data = event.html/elements/data;
```

## <span>Return Value</span>

Returns an object of type anyany

The content of the message.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

This property contains the value passed to [**postMessage**](/dom/Window/postMessage). Before trusting the data, check the [**URL**](/dom/Window/URL) property of the message request to determine its source.