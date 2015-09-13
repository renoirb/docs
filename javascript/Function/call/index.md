---
title: call
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/h2ak8h2y(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Calls a method of an object, substituting another object for the current object.'
tags:
  - JS
  - Basic
uri: javascript/Function/call

---
## <span>Summary</span>

Calls a method of an object, substituting another object for the current object.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    call([ thisObj [, arg1 [ , arg2 [ ,   [ , argN ]]]]])

**thisObj**
:   Optional. The object to be used as the current object.

**arg1, arg2, , argN**
:   Optional. A list of arguments to be passed to the method.

## <span>Examples</span>

The following code shows how to use the **call** method.

``` js
function callMe(arg1, arg2){
     var s = "";

     s += "this value: " + this;
     s += "<br />";
     for (i in callMe.arguments) {
         s += "arguments: " + callMe.arguments[i];
         s += "<br />";
     }
     return s;
 }

 document.write("Original function: <br/>");
 document.write(callMe(1, 2));
 document.write("<br/>");

 document.write("Function called with call: <br/>");
 document.write(callMe.call(3, 4, 5));

 // Output:
 // Original function:
 // this value: [object Window]
 // arguments: 1
 // arguments: 2

 // Function called with call:
 // this value: 3
 // arguments: 4
 // arguments: 5
```

## <span>Remarks</span>

The **call** method is used to call a method on behalf of another object. It allows you to change the this object of a function from the original context to the new object specified by thisObj.

If thisObj is not supplied, the global object is used as thisObj.

## <span>See also</span>

### <span>Other articles</span>

-   [Function Object](/javascript/Function)
-   [apply Method (Function)](/javascript/Function/apply)

