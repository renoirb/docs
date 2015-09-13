---
title: ScriptProcessorNode
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
summary: "This interface is an AudioNode which can generate, process, or analyse audio directly using JavaScript.\n"
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/ScriptProcessorNode

---
## <span>Summary</span>

This interface is an AudioNode which can generate, process, or analyse audio directly using JavaScript.

**Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

## <span>Properties</span>

API Name
:   Summary

[bufferSize](/apis/webaudio/ScriptProcessorNode/bufferSize)
:   The size of the buffer (in sample-frames) which needs to be processed each time [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) is called. Legal values are 256, 512, 1024, 2048, 4096, 8192, and 16384.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[onaudioprocess](/apis/webaudio/ScriptProcessorNode/onaudioprocess)
:   An event listener which is called periodically for audio processing. An event of type [**AudioProcessingEvent**](/apis/webaudio/AudioProcessingEvent) will be passed to the event handler.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
