---
title: knee
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/DynamicsCompressorNode
    href: /apis/webaudio/DynamicsCompressorNode
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/DynamicsCompressorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'A decibel value representing the range above the threshold where the curve smoothly transitions to the ratio portion. Its default value is 30, with a nominal range of 0 to 40. This parameter is k-rate.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/DynamicsCompressorNode/knee

---
## <span>Summary</span>

A decibel value representing the range above the threshold where the curve smoothly transitions to the ratio portion. Its default value is 30, with a nominal range of 0 to 40. This parameter is k-rate.

Property of [apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)[apis/webaudio/DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = DynamicsCompressorNode.knee;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var compressor = audioCtx.createDynamicsCompressor();
compressor.knee.value = 40;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
