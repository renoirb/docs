---
title: bgSound
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLBGSoundElement](/dom/HTMLBGSoundElement)'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'The bgsound element (&lt;bgsound&gt;) instructs the browser to load and play a sound file while the user is on that page. Don''t use it. Use the audio element instead.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
uri: html/elements/bgSound

---
## <span>Summary</span>

The bgsound element (&lt;bgsound&gt;) instructs the browser to load and play a sound file while the user is on that page. Don't use it. Use the audio element instead.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLBGSoundElement](/dom/HTMLBGSoundElement)

## <span>Examples</span>

If you want to use sound, please use the [audio](/html/elements/audio) element:

``` html


<audio autoplay id="bgsound">
 <source src="http://media.w3.org/2010/07/bunny/04-Death_Becomes_Fur.mp4"
         type="audio/mp4">
 <source src="http://media.w3.org/2010/07/bunny/04-Death_Becomes_Fur.oga"
         type="audio/ogg; codecs=vorbis">
 <p>Your user agent does not support the HTML5 Audio element.</p>
</audio>
<button type="button"
        onclick="document.getElementById('bgsound').pause();">
  Stop background sound
</button>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

The `<bgSound>` element can appear anywhere within the document. This element is not rendered. This element does not require a closing tag. Do not use it! In HTML5 the `<bgSound>` is described as ["non-conforming feature"](http://www.w3.org/TR/html5/obsolete.html#non-conforming-features).

### <span>Standards information</span>

There are no standards that apply here.

### <span>HTML information</span>

{

## <span>See also</span>

### <span>Related articles</span>

#### <span>Audio</span>

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [Web Audio API](/apis/webaudio)

-   [value](/apis/webaudio/AudioParam/value)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   **bgSound**

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)
