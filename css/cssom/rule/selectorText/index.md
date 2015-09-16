---
title: selectorText
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/rule
    href: /css/cssom/rule
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/rule/selectorText

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/rule](/css/cssom/rule)[css/cssom/rule](/css/cssom/rule)

## Syntax

``` js
var result = element.selectorText;
element.selectorText = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Selector text can contain either a simple selector (such as 'H1') or a contextual selector (such as 'P EM') that consists of several simple selectors. Compound selectors (such as 'B, STRONG') are stored as separate rules in the collection.

### Syntax

## See also

### Related pages

-   `rule`
-   `<b/>`
-   `IHTMLStyleSheetRulesCollection`
-   `rules`
