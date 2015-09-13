---
title: select
attributions:
  - 'Microsoft Developer Network: [[select Method](http://msdn.microsoft.com/en-us/library/ie/ms536735(v=vs.85).aspx) Article]'
notes:
  - 'Not sure if this http://www.w3.org/TR/DOM-Level-2-HTML/html is a standard or not.... the MSDN doco has not w3 ref.... see Elliot/MSFT.'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TextRange
standardization_status: 'W3C Recommendation'
summary: 'Makes the selection equal to the current object. '
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/select

---
## <span>Summary</span>

Makes the selection equal to the current object.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## <span>Syntax</span>

``` js
var result = range.select();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

When applied to a TextRange object, the select method causes the current object to be highlighted. The following function uses the findText method to set the current object to the text in the TextRange object. The function assumes an element that contains the text string "text here".

``` js
function TextRangeSelect() {
    var r = document.body.createTextRange();
    r.findText("text here");
    r.select();
}
```

When applied to a controlRange collection, the select method produces a shaded rectangle around the elements in the controlRange. The following function uses the add method to set the current object to an element in the controlRange collection. The function assumes an element with an id of "aaa".

``` js
function ControlRangeSelect() {
    var r = document.body.createControlRange();
    r.add(document.all.aaa);
    r.select();
}
```

## <span>Usage</span>

     Used to programmatically select/highlight text and/or controls in a web document.

## <span>Notes</span>

### <span>Remarks</span>

This method causes the current object to be highlighted. When applied to a [**TextRange**](/dom/TextRange) object, the select method causes the current object to be highlighted. The following function uses the **findText** method to set the current object to the text in the **TextRange** object. The function assumes an element that contains the text string "text here".

    function TextRangeSelect() {
        var r = document.body.createTextRange();
        r.findText("text here");
        r.select();
    }

This method produces a shaded rectangle around the elements in the [**controlRange**](/dom/HTMLElement/controlRange). When applied to a **controlRange** collection, the select method produces a shaded rectangle around the elements in the **controlRange**. The following function uses the add method to set the current object to an element in the **controlRange** collection. The function assumes an element with an id of "aaa".

    function ControlRangeSelect() {
        var r = document.body.createControlRange();
        r.add(document.all.aaa);
        r.select();
    }

This feature might not be available on non-Microsoft Win32 platforms.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
