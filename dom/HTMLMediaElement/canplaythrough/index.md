---
title: canplaythrough
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, clean-up of MSDN import'
readiness: 'In Progress'
summary: 'Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.'
tags:
  - Events
  - API
  - Audio
  - DOM
  - Video
uri: dom/HTMLMediaElement/canplaythrough

---
## <span>Summary</span>

Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.

## <span>Overview Table</span>

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
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## <span>Notes</span>

The **oncanplaythrough** event is raised when data is being fetched at a rate that would allow playback without interruption at the [**defaultPlaybackRate**](/dom/HTMLMediaElement/defaultPlaybackRate). If the [**autoplay**](/dom/HTMLMediaElement/autoplay) attribute is specified, the video starts playing when **oncanplaythrough** is received. This event occurs after [**oncanplay**](/dom/HTMLMediaElement/canplay) and before the first [**onprogress**](/dom/HTMLMediaElement/progress) event is received. To invoke this event, load a media resource.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.9.12

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## <span>Related specifications</span>

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
