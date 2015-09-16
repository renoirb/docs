---
title: :last-child
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/0b959135eaa76a5de965'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The :last-child pseudo-class represents the last child element of its parent.'
tags:
  - CSS
  - Selectors
uri: 'css/selectors/pseudo-classes/:last-child'

---
## Summary

The :last-child pseudo-class represents the last child element of its parent.

## Examples

``` css
/*We add some red color to the second list item*/

li:last-child {
color: red;
}
```

[View live example](http://code.webplatform.org/gist/0b959135eaa76a5de965)

``` html
<ul>
    <li>I'm not red!</li>
    <li>I'm red!</li>
</ul>
```

## Notes

### Remarks

The **:last-child** pseudo-class is a structural pseudo-class. Structural pseudo-classes enable selection based on extra information in the document tree that can't be selected using simple selectors or combinators.

### Syntax

selector

<dl>
<dd>
last-child

</dd>
</dl>
### Parameters

*selector*
:   A CSS simple selector.

### Standards information

-   [Selectors Level 3](http://go.microsoft.com/fwlink/p/?linkid=199783), Section 6.6.5.7

## Related specifications

[CSS Selectors Level 3](http://www.w3.org/TR/css3-selectors/)
:   W3C Recommendation

## See also

### Related pages (MSDN)

-   `Reference`
-   `:root`
-   `:nth-child`
-   `:nth-last-child`
-   `:nth-of-type`
-   `:nth-last-of-type`
-   `:first-of-type`
-   `:last-of-type`
-   `:only-child`
-   `:only-of-type`
-   `:empty`
