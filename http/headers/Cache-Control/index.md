---
title: Cache-Control
overview_table:
  Direction: 'Request and Response'
  Features: ''
summary: "Specifies directives for caches along the path to the origin server. The header is found in both directions, but the directives may have different semantics depending on direction.\n"
tags:
  - HTTP
  - Headers
uri: http/headers/Cache-Control

---
## Summary

Specifies directives for caches along the path to the origin server. The header is found in both directions, but the directives may have different semantics depending on direction.

Request directives are:

-   max-age
-   max-stale
-   min-fresh
-   no-cache
-   no-store
-   no-transform
-   only-if-cached

Response directives are:

-   must-revalidate
-   no-cache
-   no-store
-   no-transform
-   public
-   private
-   proxy-revalidate
-   max-age
-   s-maxage

## Overview table

Direction
:   Request and Response

Features
:

## Syntax

    Cache-Control   = 1#cache-directive
    cache-directive = token [ "=" ( token / quoted-string ) ]

## Examples

``` html

```

## Related specifications

[RFC7234: HTTP/1.1 Caching](http://tools.ietf.org/html/rfc7234#section-5.2)
:

