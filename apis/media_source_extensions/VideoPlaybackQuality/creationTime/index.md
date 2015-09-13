---
title: creationTime
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/media_source_extensions/VideoPlaybackQuality
    href: /apis/media_source_extensions/VideoPlaybackQuality
  return:
    predicate: 'Returns an object of type '
    value: VARIANT
    href: /apis/media_source_extensions/VideoPlaybackQuality
standardization_status: 'W3C Editor''s Draft'
summary: 'Gets the timestamp for when the VideoPlaybackQuality metrics were collected.'
tags:
  - API
  - Object
  - Properties
uri: 'apis/media source extensions/VideoPlaybackQuality/creationTime'

---
## <span>Summary</span>

Gets the timestamp for when the VideoPlaybackQuality metrics were collected.

Property of [apis/media\_source\_extensions/VideoPlaybackQuality](/apis/media_source_extensions/VideoPlaybackQuality)[apis/media\_source\_extensions/VideoPlaybackQuality](/apis/media_source_extensions/VideoPlaybackQuality)

## <span>Syntax</span>

``` js
var time = VideoPlaybackQuality.creationTime;
VideoPlaybackQuality.creationTime = time;
```

## <span>Return Value</span>

Returns an object of type VARIANTVARIANT

Type: DOMHighResTimeStamp The timestamp for when the quality metrics were collected.

**Needs Examples**: This section should include examples.

