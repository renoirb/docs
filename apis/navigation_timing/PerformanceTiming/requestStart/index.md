---
title: requestStart
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: 'apis/navigation timing/PerformanceTiming'
    href: /apis/navigation_timing/PerformanceTiming
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/navigation_timing/PerformanceTiming
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.'
tags:
  0: API
  1: Object
  2: Properties
  4: Navigation
  5: Timing
uri: 'apis/navigation timing/PerformanceTiming/requestStart'

---
## <span>Summary</span>

Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.

Property of [apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)[apis/navigation timing/PerformanceTiming](/apis/navigation_timing/PerformanceTiming)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = PerformanceTiming.requestStart;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

``` js
var perftime = performance.timing;
document.write("requestStart: " + perftime.requestStart + "<br />");
```

## <span>Notes</span>

The PerformanceTiming interface does not include an attribute to represent the completion of sending the request, e.g., requestEnd.

-   Completion of sending the request from the user agent does not always indicate the corresponding completion time in the network transport, which brings most of the benefit of having such an attribute.
-   Some user agents have high cost to determine the actual completion time of sending the request due to the HTTP layer encapsulation.

## <span>Related specifications</span>

[Navigation Timing 2](http://www.w3.org/TR/navigation-timing-2/)
:   W3C Working Draft
