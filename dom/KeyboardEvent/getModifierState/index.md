---
title: getModifierState
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'example/more description, compatibility'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/KeyboardEvent
    href: /dom/KeyboardEvent
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/KeyboardEvent
standardization_status: 'W3C Working Draft'
summary: 'Queries the state of the specified modifier key.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/KeyboardEvent/getModifierState

---
## <span>Summary</span>

Queries the state of the specified modifier key.

Method of [dom/KeyboardEvent](/dom/KeyboardEvent)[dom/KeyboardEvent](/dom/KeyboardEvent)

## <span>Syntax</span>

``` js
var modifierState = event.getModifierState(modifierKeyName);
```

## <span>Parameters</span>

### <span>modifierKeyName</span>

 Data-type
:   String

 One of the following values -

-   **Alt** - The left or right Alt key.
-   **AltGraph** - The Ctrl and Alt keys.
-   **CapsLock** - The Caps Lock toggle.
-   **Control** - The left or right Ctrl key.
-   **Meta** - The Meta/Control key.
-   **NumLock** - The Num Lock toggle.
-   **ScrollLock** - The Scroll Lock toggle.
-   **Shift** - The left or right Shift key.
-   **Fn**
-   **OS**
-   **SymbolLock**

Other implementation specific options may be supported. For example -

-   **Win** (on Microsoft Windows) - The left or right Windows logo key.
-   **Scroll** - The Scroll Lock toggle.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the modifier key is active.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Some keyboard configurations contain a left and right modifier key. To determine whether the left or right key is pressed, use the [**location**](/dom/KeyboardEvent/location) property.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
