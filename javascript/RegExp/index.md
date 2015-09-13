---
title: RegExp
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9dthzd08(v=vs.94).aspx)'
notes:
  - 'Todo: Replace manual properties and methods tables with generated tables.'
readiness: 'Ready to Use'
summary: 'An intrinsic global object that stores information about the results of regular expression pattern matches.'
tags:
  0: JS
  1: Basic
  3: Object
uri: javascript/RegExp

---
## <span>Summary</span>

An intrinsic global object that stores information about the results of regular expression pattern matches.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    RegExp.property

## <span>Examples</span>

The following example performs a regular expression search. It displays matches and submatches from the global `RegExp` object, and from the array that is returned by the `exec` method.

``` js
var newLine = "<br />";

 var re = /(\w+)@(\w+)\.(\w+)/g
 var src = "Please send mail to george@contoso.com and someone@example.com. Thanks!"

 var result;
 var s = "";

 // Get the first match.
 result = re.exec(src);

 while (result != null) {
     // Show the entire match.
     s += newLine;

     // Show the match and submatches from the RegExp global object.
     s += "RegExp.lastMatch: " + RegExp.lastMatch + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;

     // Show the match and submatches from the array that is returned
     // by the exec method.
     for (var index = 0; index < result.length; index++) {
         s +=  index + ": ";
         s += result[index];
         s += newLine;
     }

     // Get the next match.
     result = re.exec(src);
 }
 document.write(s);

 // Output:
 //  RegExp.lastMatch: george@contoso.com
 //  RegExp.: george
 //  RegExp.: contoso
 //  RegExp.: com
 //  0: george@contoso.com
 //  1: george
 //  2: contoso
 //  3: com

 //  RegExp.lastMatch: someone@example.com
 //  RegExp.: someone
 //  RegExp.: example
 //  RegExp.: com
 //  0: someone@example.com
 //  1: someone
 //  2: example
 //  3: com
```

## <span>Remarks</span>

The required property argument can be any one of the `RegExp` object properties.

The `RegExp` object cannot be created directly, but is always available for use. Until a successful regular expression search has been completed, the initial values of the various properties of the `RegExp` object are as follows:

|Property|Shorthand|Initial Value|
|:-------|:--------|:------------|
|[index](/javascript/RegExp/index)|-1|(none)|
|[input](/javascript/RegExp/input)|\$\_|Empty string.|
|[lastIndex](/javascript/RegExp/lastIndex)|-1|(none)|
|[lastMatch](/javascript/RegExp/lastMatch)|\$&|Empty string.|
|[lastParen](/javascript/RegExp/lastParen)|\$+|Empty string.|
|[leftContext](/javascript/RegExp/leftContext)|\$\`|Empty string.|
|[rightContext](/javascript/RegExp/rightContext)|\$'|Empty string.|
|[\$1 - \$9](/javascript/RegExp/1_9_Properties)|\$1 - \$9|Empty string.|

Its properties have undefined as their value until a successful regular expression search has been completed.

The global `RegExp` object should not be confused with the **Regular Expression** object. Even though they sound like the same thing, they are separate and distinct. The properties of the global `RegExp` object contain continually updated information about each match as it occurs, while the properties of the **Regular Expression** object contain only information about the matches that occur with that instance of the **Regular Expression**.

## <span>Properties</span>

||
|[global](/javascript/RegExp/global)|Returns a Boolean value indicating the state of the global flag ( g ) used with a regular expression.|
|[ignoreCase](/javascript/RegExp/ignoreCase)|Returns a Boolean value indicating the state of the ignoreCase flag ( i ) used with a regular expression.|
|[multiline](/javascript/RegExp/multiline)|Returns a Boolean value indicating the state of the multiline flag ( m ) used with a regular expression.|
|[source](/javascript/RegExp/source)|Returns a copy of the text of the regular expression pattern.|
|[sticky](/javascript/RegExp/sticky)|Returns a Boolean value indicating the state of the sticky flag ( y ) used with a regular expression.|
|[unicode](/javascript/RegExp/unicode)|Returns a Boolean value indicating the state of the Unicode flag (u) used with a regular expression.|

## <span>Methods</span>

||
|[compile](/javascript/RegExp/compile)|Compiles a regular expression into an internal format for faster execution.|
|[exec](/javascript/RegExp/exec)|Executes a search on a string using a regular expression pattern, and returns an array containing the results of that search.|
|[test](/javascript/RegExp/test)|Returns a Boolean value that indicates whether or not a pattern exists in a searched string.|

## <span>Properties</span>

The following table lists the properties of the **RegExp** object.

|Property|Summary|
|:-------|:------|
|[global](/javascript/RegExp/global)|Returns a Boolean value indicating the state of the global flag ( **g** ) used with a regular expression. Default is **false**. Read-only.|
|[ignoreCase](/javascript/RegExp/ignoreCase)|Returns a Boolean value indicating the state of the ignoreCase flag ( **i** ) used with a regular expression. Default is **false**. Read-only.|
|[multiline](/javascript/RegExp/multiline)|Returns a Boolean value indicating the state of the multiline flag ( **m** ) used with a regular expression. Default is **false**. Read-only.|
|[source](/javascript/RegExp/source)|Returns a copy of the text of the regular expression pattern. Read-only. The rgExp argument is a **Regular expression** object. It can be a variable name or a literal.|
|[sticky](/javascript/RegExp/sticky)|Returns a Boolean value indicating the state of the sticky flag ( **y** ) used with a regular expression. Default is `false`. Read-only.|
|[unicode](/javascript/RegExp/unicode)|Returns a Boolean value indicating the state of the Unicode flag (`u`) used with a regular expression. Default is `false`. Read-only.|

## <span>Functions</span>

The following table lists the functions of the **RegExp** object.

## <span>Methods</span>

The following table lists the methods of the **RegExp** object.

|Method|Summary|
|:-----|:------|
|[compile](/javascript/RegExp/compile)|Compiles a regular expression into an internal format for faster execution.|
|[exec](/javascript/RegExp/exec)|Executes a search on a string using a regular expression pattern, and returns an array containing the results of that search.|
|[test](/javascript/RegExp/test)|Returns a Boolean value that indicates whether or not a pattern exists in a searched string.|

## <span>See also</span>

### <span>Other articles</span>

-   [Regular Expression Object](/javascript/regular_expression)
-   [String Object](/javascript/String)

