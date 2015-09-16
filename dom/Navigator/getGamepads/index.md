---
title: getGamepads
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.getGamepads method](https://developer.mozilla.org/en-US/docs/Web/API/Navigator.getGamepads) Article]'
  - 'Microsoft Developer Network: [[Gamepad API in DevChannel](http://msdn.microsoft.com/en-us/library/ie/dn753843(v=vs.85).aspx) Article]'
notes:
  - 'MSDN documentation only available on devChannel.'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Navigator
    href: /dom/Navigator
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /dom/Navigator
standardization_status: 'W3C Working Draft'
summary: 'Retrieves a snapshot of the data for the currently connected and interacted-with gamepads. Returns a Gamepad object.'
tags:
  0: API
  1: Object
  2: Methods
  4: Gamepad
uri: dom/Navigator/getGamepads

---
## Summary

Retrieves a snapshot of the data for the currently connected and interacted-with gamepads. Returns a Gamepad object.

Method of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

``` js
var result = navigator.getGamepads();
```

## Return Value

Returns an object of type

gamePads collection.

## Examples

This example detects when a gamepad is connected to the computer.

``` js
window.addEventListener("gamepadconnected", function(e) {
  var gp = navigator.getGamepads()[0];
  console.log("Gamepad connected at index %d: %s. %d buttons, %d axes.",
  gp.index, gp.id,
  gp.buttons.length, gp.axes.length);
});
```

## Related specifications

[W3C Gamepad Specification](https://dvcs.w3.org/hg/gamepad/raw-file/default/gamepad.html)
:   W3C Working Draft
