---
title: window.location.hostname
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/location
    href: /apis/location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/location
standardization_status: 'W3C Working Draft'
summary: 'The hostname property contains the hostname the current document was served from, excluding protocol, port, and other information.'
tags:
  - API
  - Object
  - Properties
  - JavaScript
uri: apis/location/hostname

---
## <span>Summary</span>

The hostname property contains the hostname the current document was served from, excluding protocol, port, and other information.

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = window.location.hostname;
```

## <span>Return Value</span>

Returns an object of type StringString

The hostname the current document was served from.

For example, `http://example.org/` would return the hostname `example.org`.

## <span>Examples</span>

The following example assumes your document has a div element with id 'hostDiv', like this.

``` js
// Get the hostname from window.location
var hostnm = window.location.hostname;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the hostname
container.innerHTML = hostnm;
```

## <span>Related specifications</span>

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
