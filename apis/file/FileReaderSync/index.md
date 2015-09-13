---
title: FileReaderSync
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Allows for synchronous reading of File or Blob objects. Only available in Workers, as synchronous I/O would otherwise block the main application from executing.'
tags:
  0: API
  1: Objects
  3: FileAPI
uri: apis/file/FileReaderSync

---
## <span>Summary</span>

Allows for synchronous reading of File or Blob objects. Only available in Workers, as synchronous I/O would otherwise block the main application from executing.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Notes</span>

**Important:**  The FileReaderSync object's read methods (readAsText, readAsDataURL, and readAsArrayBuffer) have the same method signatures as the read methods of the [FileReader](/apis/file/FileReader) object but they behave synchronously (as opposed to asynchronously).

## <span>Related specifications</span>

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
