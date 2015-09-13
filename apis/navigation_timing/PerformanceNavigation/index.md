---
title: PerformanceNavigation
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An interface that provides Web applications with navigation-related information.'
tags:
  0: API
  1: Objects
  3: Navigation
  4: Timing
uri: 'apis/navigation timing/PerformanceNavigation'

---
## <span>Summary</span>

An interface that provides Web applications with navigation-related information.

## <span>Properties</span>

API Name
:   Summary

[redirectCount](/apis/navigation_timing/PerformanceNavigation/redirectCount)
:   Returns the number of redirects since the last non-redirect navigation under the current browsing context. If there is no redirect or there is any redirect that is not from the same origin as the destination document, returns zero.

[type](/apis/navigation_timing/PerformanceNavigation/type)
:   Returns the type of the last non-redirect navigation in the current browsing context. See Notes.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C Navigation Timing Specification](http://w3c-test.org/webperf/specs/NavigationTiming/)
:   W3C Editor's Draft
