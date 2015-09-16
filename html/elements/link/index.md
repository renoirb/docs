---
title: link
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Discussion on semantics of hyperlinks'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLLinkElement](/dom/HTMLLinkElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'Enables the current document to establish links to external documents.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/link

---
## Summary

Enables the current document to establish links to external documents.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLLinkElement](/dom/HTMLLinkElement)

The \<link\> element allows authors to link their document to other resources. It carries the same semantics as any hyperlink, or the HTTP `Link:` header.

## Attributes

-   `href` = URL potentially surrounded by spaces
    Specifies a URL that provides the destination of the link.
-   `rel` = set of space-separated tokens
    Specifies a list of tokens that specify the relationship between the document containing the link and the destination indicated by the link.Two categories of links can be created using the link element: Links to external resources and hyperlinks:
-   `media` = media-query list
    The media for which the destination of the hyperlink was designed.
    If the link is a hyperlink then the media attribute is purely advisory, and describes for which media the document in question was designed.
    However, if the link is an external resource link, then the media attribute is prescriptive. The user agent must apply the external resource when the media attribute's value matches the environment and the other relevant conditions apply, and must not apply it otherwise.
    The default, if the media attribute is omitted, is "all", meaning that by default links apply to all media.
-   `hreflang` = language tag
    The language of the destination of the hyperlink.
    A valid language tag, as defined in [BCP47].
-   `type` = A valid MIME type that destination of the hyperlink.
    gives the MIME type of the linked resource.
    The default value for the type attribute, which is used if the attribute is absent, is "text/css".
-   `sizes` = icon sizes
    The sizes attribute is used with the icon link type. The attribute must not be specified on link elements that do not have a rel attribute that specifies the icon keyword.
-   Also, the title attribute has special semantics on this element. The exception is for style sheet links, where the title attribute defines alternative style sheet sets.

## Link relations

A URI or any IANA Link can be used as the link `rel=""`, but HTML defines special semantics for many of them:

|Link type|Category|Description|
|:--------|:-------|:----------|
|alternate|Hyperlink|Gives alternate representations of the current document.|
|archives|Hyperlink|Provides a link to a collection of records, documents, or other materials of historical interest.|
|author|Hyperlink|Gives a link to the current document's author.|
|first|Hyperlink|Indicates that the current document is a part of a series, and that the first document in the series is the referenced document.|
|help|Hyperlink|Provides a link to context-sensitive help.|
|icon|External Resource|Imports an icon to represent the current document.|
|index|Hyperlink|Gives a link to the document that provides a table of contents or index listing the current document.|
|last|Hyperlink|Indicates that the current document is a part of a series, and that the last document in the series is the referenced document.|
|license|Hyperlink|Indicates that the main content of the current document is covered by the copyright license described by the referenced document.|
|next|Hyperlink|Indicates that the current document is a part of a series, and that the next document in the series is the referenced document.|
|pingback|External Resource|Gives the address of the pingback server that handles pingbacks to the current document.|
|prefetch|External Resource|Specifies that the target resource should be preemptively cached.|
|prev|Hyperlink|Indicates that the current document is a part of a series, and that the previous document in the series is the referenced document.|
|search|Hyperlink|Gives a link to a resource that can be used to search through the current document and its related pages.|
|stylesheet|External Resource|Imports a stylesheet.|
|sidebar|Hyperlink|Specifies that the referenced document, if retrieved, is intended to be shown in the browser's sidebar (if it has one).|
|tag|Hyperlink|Gives a tag (identified by the given address) that applies to the current document.|
|up|Hyperlink|Provides a link to a document giving the context for the current document.|

## Examples

This example uses the **link** element to apply an external style sheet, called styles.css, to the page.

``` html
<link rel=stylesheet href="styles.css" type="text/css"/>
```

## Notes

### Remarks

The **link** element can be used only within the **head** tag. Windows Internet Explorer 8 and later. The behavior of the [**href**](/html/attributes/href) and the [**rel**](/html/attributes/rel) attributes depends on the current document compatibility mode.

### IANA Link Relations database

The IANA maintains a registry of valid link relations at their [Link Relations registry](http://www.iana.org/assignments/link-relations/link-relations.xhtml), established in [RFC5988](https://tools.ietf.org/html/rfc5988).

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-link-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-link-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/links.html#edef-LINK)
:   W3C Recommendation

[RFC 5988: Web Linking](https://tools.ietf.org/html/rfc5988)
:   Standards Track

[Subresource Integrity](http://www.w3.org/TR/SRI/)
:   W3C Working Draft
