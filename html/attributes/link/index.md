---
title: link
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Enables the current document to establish links to external documents.'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/linkColor
uri: html/attributes/link

---
## Summary

Enables the current document to establish links to external documents.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **link** property cannot be set through the **BODY** object's [**onload**](/dom/events/load) event, but the [**linkColor**](/w/index.php?title=dom/properties/linkColor&action=edit&redlink=1) property can. Some browsers do not recognize color names, but all browsers should recognize RGB color values and display them correctly.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 7.5.1 (Deprecated)

## See also

### Related pages (MSDN)

-   `body`
