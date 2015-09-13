---
title: initMouseEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'compatibility, examples'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new mouse event that the  createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
uri: dom/MouseEvent/initMouseEvent

---
## <span>Summary</span>

Initializes a new mouse event that the createEvent method created.

Method of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## <span>Syntax</span>

``` js
 event.initMouseEvent(eventType, canBubble, cancelable, view, detail, screenX, screenY, clientX, clientY, ctrlKey, altKey, shiftKey, metaKey, button, relatedTarget);
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

### <span>view</span>

 Data-type
:   DOM Node

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### <span>detail</span>

 Data-type
:   Number

 Specifies additional information. This value is returned in the [**detail**](/dom/UIEvent/detail) property of the event.

### <span>screenX</span>

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the screen. Sets the value for the [**screenX**](/dom/MouseEvent/screenX) property,

### <span>screenY</span>

 Data-type
:   Number

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the screen. Sets the value for the [**screenY**](/dom/MouseEvent/screenY) property.

### <span>clientX</span>

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. Sets the value for the [**clientX**](/dom/MouseEvent/clientX) property.

### <span>clientY</span>

 Data-type
:   Number

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. Sets the value for the [**clientY**](/dom/MouseEvent/clientY) property.

### <span>ctrlKey</span>

 Data-type
:   Boolean

 Whether the Control key is depressed. Sets the value for the [**ctrlKey**](/dom/KeyboardEvent/ctrlKey) property.

### <span>altKey</span>

 Data-type
:   Boolean

 Whether the Alt key is depressed. Sets the value for the [**altKey**](/dom/KeyboardEvent/altKey) property.

### <span>shiftKey</span>

 Data-type
:   Boolean

 Whether the Shift key is depressed. Sets the value for the [**shiftKey**](/dom/KeyboardEvent/shiftKey) property.

### <span>metaKey</span>

 Data-type
:   Boolean

 Whether a meta key is depressed. Sets the value for the [**metaKey**](/dom/KeyboardEvent/metaKey) property.

### <span>button</span>

 Data-type
:   Number

 The mouse button that caused the event. Sets the value for the [**button**](/dom/MouseEvent/button) property (see the property page for common values).

### <span>relatedTarget</span>

 Data-type
:   DOM Node

 A secondary element that is involved in the event. Sets the value for the [**relatedTarget**](/dom/MouseEvent/relatedTarget) property.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
