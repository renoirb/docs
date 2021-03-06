---
title: startTime
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: 'apis/user timing/PerformanceMeasure'
    href: /apis/user_timing/PerformanceMeasure
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/user_timing/PerformanceMeasure
standardization_status: 'W3C Recommendation'
summary: 'Returns a DOMHighResTimeStamp with the measure''s High Resolution Time start mark.'
tags:
  0: API
  1: Object
  2: Properties
  4: User
  5: Timing
uri: 'apis/user timing/PerformanceMeasure/startTime'

---
## Summary

Returns a DOMHighResTimeStamp with the measure's High Resolution Time start mark.

Property of [apis/user timing/PerformanceMeasure](/apis/user_timing/PerformanceMeasure)[apis/user timing/PerformanceMeasure](/apis/user_timing/PerformanceMeasure)

## Syntax

``` js
var result = element.startTime;
element.startTime = value;
```

## Return Value

Returns an object of type

DOMHighResTimeStamp

## Examples

``` js
// set begin mark
performance.mark("startMark");
// execute a function to be measured
someFunction();
// set end mark
performance.mark("stopMark");

// save the timing information
performance.measure("functionTime", "startMark", "stopMark");
// display the measure's data
var measures = performance.getEntriesByType("measure");
alert("Measure name: " + measures[0].name + "\n" +
      "Measure type: " + measures[0].entryType + "\n" +
      "Measure start: " + measures[0].startTime + "\n" +
      "Measure duration: " + measures[0].duration);

// clear the measure "functionTime"
performance.clearMeasures("functionTime");
// clear all marks
performance.clearMarks();
```

## Related specifications

[W3C User Timing Specification](http://www.w3.org/TR/user-timing/)
:   W3C Recommendation
