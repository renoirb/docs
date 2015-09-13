---
title: setHours
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/f4a5xhxy(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the hour value in the Date object using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setHours

---
## <span>Summary</span>

Sets the hour value in the Date object using local time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.setHours( numHours [ , numMin [ , numSec [ , numMilli ]]] )

**dateObj**
:   Required. Any Date object.

**numHours**
:   Required. A numeric value equal to the hours value.

**numMin**
:   Optional. A numeric value equal to the minutes value. Must be supplied if either of the following arguments is used.

**numSec**
:   Optional. A numeric value equal to the seconds value. Must be supplied if the following argument is used.

**numMilli**
:   Optional. A numeric value equal to the milliseconds value.

## <span>Examples</span>

The following example illustrates the use of the **setHours** method.

``` js
function SetHoursDemo(nhr, nmin, nsec){
    var d, s;                     //Declare variables.
    d = new Date();               //Create Date object.d.setHours( nhr , nmin , nsec ) ;  //Set hours, minutes, & seconds.
    s = "Current setting is " + d.toLocaleString()
    return(s);                    //Return new date setting.
 }
```

## <span>Remarks</span>

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numMinutes argument is not specified, JavaScript uses the value returned from the **getMinutes** method.

To set the hours value using Universal Coordinated Time (UTC), use the **setUTCHours** method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00", and **setHours(30)** is called, the date is changed to "Jan 6, 1996 06:00:00." Negative numbers have a similar behavior.

## <span>See also</span>

### <span>Other articles</span>

-   [getHours Method (Date)](/javascript/Date/getHours)
-   [getUTCHours Method (Date)](/javascript/Date/getUTCHours)
-   [setUTCHours Method (Date)](/javascript/Date/setUTCHours)

