---
title: constructor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155297(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Specifies the function that creates a string.'
tags:
  - JS
  - Basic
uri: javascript/String/constructor

---
## <span>Summary</span>

Specifies the function that creates a string.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    string.constructor

## <span>Examples</span>

The following example illustrates the use of the constructor property.

``` js
var x = new String();

 if (x.constructor == String)
     document.write("Object is a String.");
 else
     document.write("Object is not a String.");

 // Output:
 // Object is a String.
```

## <span>Remarks</span>

The required string is the name of a string.

The **constructor** property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the **Global** and **Math** objects. The **constructor** property contains a reference to the function that constructs instances of that particular object.

