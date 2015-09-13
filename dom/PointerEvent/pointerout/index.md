---
title: pointerout
attributions:
  - 'Microsoft Developer Network: [[pointerout Event](http://msdn.microsoft.com/en-us/library/ie/hh771912(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "Dispatched when any of the following occurs:\n"
tags:
  - Events
  - DOM
uri: dom/PointerEvent/pointerout

---
## <span>Summary</span>

Dispatched when any of the following occurs:

-   A pointing device is moved out of the hit test boundaries of an element
-   After firing the [pointerup](/dom/PointerEvent/pointerup) event for a device that does not support hover
-   After firing the [pointercancel](/dom/PointerEvent/pointercancel) event

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

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
Varies: when the pointer is primary, all default actions of the [mouseout](/dom/MouseEvent/mouseout) event

</td>
</tr>
</table>
## <span>Examples</span>

``` js
element.addEventListener("pointerout", handler, useCapture) ;
```

## <span>Related specifications</span>

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft
