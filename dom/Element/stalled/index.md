---
title: stalled
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, and compat, also better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/Element/stalled

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

This event occurs if three seconds have passed since the last packet was downloaded. To invoke this event, do one of the following:

-   Disconnect the network while the media resource is downloading.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.12

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   `audioApi`
-   `audioElement`
-   `Document`
-   `source`
-   `videoElement`
-   `videoApi`
-   `Window`
-   `waiting`
