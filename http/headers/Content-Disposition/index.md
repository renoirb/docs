---
title: Content-Disposition
overview_table:
  Direction: Response
  Features: ''
summary: 'Used to convey additional information about how to process the response payload.'
tags:
  - HTTP
  - Headers
uri: http/headers/Content-Disposition

---
## Summary

Used to convey additional information about how to process the response payload.

## Overview table

Direction
:   Response

Features
:

## Syntax

    content-disposition = "Content-Disposition" ":"
                           disposition-type *( ";" disposition-parm )

    disposition-type    = "inline" | "attachment" | disp-ext-type
                        ; case-insensitive
    disp-ext-type       = token

    disposition-parm    = filename-parm | disp-ext-parm

    filename-parm       = "filename" "=" value
                        | "filename*" "=" ext-value

    disp-ext-parm       = token "=" value
                        | ext-token "=" ext-value
    ext-token           = <the characters in token, followed by "*">

## Examples

```
Content-Disposition: Attachment; filename=example.html
```

## Notes

Content-Disposition as used in HTTP is a subset of the [same header defined in MIME](http://tools.ietf.org/html/rfc2183)

## Related specifications

[RFC6266: Use of the Content-Disposition Header Field in HTTP](http://tools.ietf.org/html/rfc6266)
:

