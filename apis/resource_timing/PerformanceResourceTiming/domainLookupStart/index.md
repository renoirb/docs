---
title: domainLookupStart
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/resource_timing/PerformanceResourceTiming
    href: /apis/resource_timing/PerformanceResourceTiming
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/resource_timing/PerformanceResourceTiming
standardization_status: 'W3C Working Draft'
summary: 'Returns the time immediately before the user agent starts the domain name lookup for the resource.'
tags:
  0: API
  1: Object
  2: Properties
  4: Resource
  5: Timing
uri: 'apis/resource timing/PerformanceResourceTiming/domainLookupStart'

---
## Summary

Returns the time immediately before the user agent starts the domain name lookup for the resource.

Property of [apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)[apis/resource\_timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.domainLookupStart;
```

## Return Value

Returns an object of type

DOMHighResTimeStamp

## Examples

This example assumes an HTML page containing a resource such as \<img src="<https://www.webplatform.org/logo/logo-with-text.png>" /\>

``` js
var resources = window.performance.getEntriesByType('resource');
alert("domainLookupStart: " + resources[0].domainLookupStart);
```

## Notes

If a page is retrieved from an application cache, **domainLookupStart** has the same value as **fetchStart**. The value reported by the **domainLookupStart** property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).

## Related specifications

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft
