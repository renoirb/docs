---
title: inputMethod
attributions:
  - 'Microsoft Developer Network: [[inputMethod Property](http://msdn.microsoft.com/en-us/library/ie/ff974806(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/TextEvent
    href: /dom/TextEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/TextEvent
summary: 'Gets a value that describes how text is entered.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/TextEvent/inputMethod

---
## <span>Summary</span>

Gets a value that describes how text is entered.

Property of [dom/TextEvent](/dom/TextEvent)[dom/TextEvent](/dom/TextEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var inputMethod = event.inputMethod;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

The input method used to generate the event. One of the following values -

-   TextEvent.DOM\_INPUT\_METHOD\_UNKNOWN = 0
-   TextEvent.DOM\_INPUT\_METHOD\_KEYBOARD = 1
-   TextEvent.DOM\_INPUT\_METHOD\_PASTE = 2
-   TextEvent.DOM\_INPUT\_METHOD\_DROP = 3
-   TextEvent.DOM\_INPUT\_METHOD\_IME = 4
-   TextEvent.DOM\_INPUT\_METHOD\_OPTION = 5
-   TextEvent.DOM\_INPUT\_METHOD\_HANDWRITING = 6
-   TextEvent.DOM\_INPUT\_METHOD\_VOICE = 7
-   TextEvent.DOM\_INPUT\_METHOD\_MULTIMODAL = 8
-   TextEvent.DOM\_INPUT\_METHOD\_SCRIPT = 9

## <span>Examples</span>

Display a user friendly value of the inputMethod property of an event.

``` js
var description=(event.inputMethod)?getDOMInputMethod(event.inputMethod):'not supported';

    function getDOMInputMethod(iInputMethod){
        switch (iInputMethod){
            case TextEvent.DOM_INPUT_METHOD_UNKNOWN:// 0
                return 'Unknown';
            case TextEvent.DOM_INPUT_METHOD_KEYBOARD:// 1
                return 'Keyboard';
            case TextEvent.DOM_INPUT_METHOD_PASTE:// 2
                return 'Paste';
            case TextEvent.DOM_INPUT_METHOD_DROP:// 3
                return 'Drop';
            case TextEvent.DOM_INPUT_METHOD_IME:// 4
                return 'IME';
            case TextEvent.DOM_INPUT_METHOD_OPTION:// 5
                return 'Option';
            case TextEvent.DOM_INPUT_METHOD_HANDWRITING:// 6
                return 'Handwriting';
            case TextEvent.DOM_INPUT_METHOD_VOICE://7
                return 'Voice';
            case TextEvent.DOM_INPUT_METHOD_MULTIMODAL: // 8
                return 'MultiModal';
            case TextEvent.DOM_INPUT_METHOD_SCRIPT://9
                return 'Script';
            default:
                return 'Unknown';
        }
    }
```

## <span>Usage</span>

     Use to determine if the device that initiated the textinput event is to be 'trusted'.

## <span>Notes</span>

Not implemented in Safari or Chromium.

## <span>Related specifications</span>

[DOM Level 3 Events (20110531)](http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531)
:   Outdated Working Draft
