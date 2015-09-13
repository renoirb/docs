---
title: AudioTrack
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'AudioTrack is an object representing an audio portion of a video element.'
tags:
  0: API
  1: Objects
  3: Audio
  4: Video
uri: apis/audio-video/AudioTrack

---
## <span>Summary</span>

AudioTrack is an object representing an audio portion of a video element.

## <span>Properties</span>

API Name
:   Summary

[enabled](/apis/audio-video/AudioTrack/enabled)
:   Returns true if the given track is active, and false otherwise. Can be set, to change whether the track is enabled or not. If multiple audio tracks are enabled simultaneously, they are mixed.

[id](/apis/audio-video/AudioTrack/id)
:   Returns the ID of the given track. This is the ID that can be used with a fragment identifier if the format supports the Media Fragments URI syntax, and that can be used with the getTrackById() method.

[kind](/apis/audio-video/AudioTrack/kind)
:   Returns the category the given track falls into.

[label](/apis/audio-video/AudioTrack/label)
:   Returns the label of the given track, if known, or the empty string otherwise.

[language](/apis/audio-video/AudioTrack/language)
:   Returns the language of the given track, if known, or the empty string otherwise.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Notes</span>

Audio tracks are represented on a **video** element as an [**AudioTrackList**](/apis/audio-video/AudioTrackList) object, which contains one or more audio tracks.

## <span>Related specifications</span>

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
