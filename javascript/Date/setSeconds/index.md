---
title: setSeconds
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/df6eb6zf(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the seconds value in the Date object using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setSeconds

---
## <span>Summary</span>

Sets the seconds value in the Date object using local time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj .setSeconds( numSeconds [ , numMilli ] )

**dateObj**
:   Required. Any Date object.

**numSeconds**
:   Required. A numeric value equal to the seconds value.

**numMilli**
:   Optional. A numeric value equal to the milliseconds value.

## <span>Examples</span>

The following example illustrates the use of the **setSeconds** method.

``` js
function SetSecondsDemo(nsec){
    var d = new Date();         //Create Date object.d.setSeconds( nsec ) ;         //Set seconds.
    var s = "Current setting is ";
    s += d.toLocaleString();
    return(s);                  //Return new setting.
 }
```

## <span>Remarks</span>

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numMilli argument is not specified, JavaScript uses the value returned from the **getMilliseconds** method.

To set the seconds value using Universal Coordinated Time (UTC), use the **setUTCSeconds** method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00" and **setSeconds(150)** is called, the date is changed to "Jan 5, 1996 00:02:30."

The setHours method can be used to set the hours, minutes, seconds, and milliseconds.

## <span>See also</span>

### <span>Other articles</span>

-   [getSeconds Method (Date)](/javascript/Date/getSeconds)
-   [getUTCSeconds Method (Date)](/javascript/Date/getUTCSeconds)
-   [setUTCSeconds Method (Date)](/javascript/Date/setUTCSeconds)

