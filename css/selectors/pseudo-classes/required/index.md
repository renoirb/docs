---
title: :required
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs title, summary, spec reference, standardization status, remove topic cluster flags'
readiness: 'Not Ready'
tags:
  - CSS
  - Selectors
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection
uri: 'css/selectors/pseudo-classes/:required'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Examples</span>

The following example puts a green border on a field when it is valid and a red border with bold text when it isn't. The email field is required, but the others aren't. The URL field is pre-filled with a bad URL, so it isn't valid when the page opens. In addition, the two optional fields are styled with light gray backgrounds, and the required field with an eye-catching yellow background.

``` html
<!DOCTYPE html >
<html>
<head>
  <title>:valid/:invalid Pseudo-class Example</title>
  <style type="text/css">

  #PC1 input:valid {
    border:solid lime;
    font-weight:normal;
  }
  #PC1 input:invalid {
    border:solid red;
    font-weight:bold;
  }
  #PC1 input:required {
    background-color:Yellow;
  }
  #PC1 input:optional {
    background-color:LightGray;
  }
  </style>
</head>
<body>
  <form id="PC1">
    <p><label>Enter some text: <input type="text"/></label></p>
    <p><label>*Enter a valid email address: <input type="email" required /></label></p>
    <p><label>Enter a valid URL: <input type="url" value="not a url"/></label></p>
    <p>* required field</p>
  </form>
</body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

A *required* field is a field that cannot be submitted without a value. A required field has the [required](http://go.microsoft.com/fwlink/p/?LinkId=233321) attribute set in its [input](http://go.microsoft.com/fwlink/p/?LinkID=219805) element. The [required](http://go.microsoft.com/fwlink/p/?LinkId=233321) attribute can be set on text, URL, email, select, checkbox, or radio button controls, and on [select](http://go.microsoft.com/fwlink/p/?LinkId=233312) and [textarea](http://go.microsoft.com/fwlink/p/?LinkID=236896) elements. It is a Boolean attribute, and need be specified only on an element. When users hover the mouse over a required field, they'll see a tooltip stating that it is a required field. (If you've set the [title](http://go.microsoft.com/fwlink/p/?LinkId=236898) attribute, that will be shown instead.)

### <span>Syntax</span>

selector

<dl>
<dd>
required

</dd>
</dl>
### <span>Parameters</span>

*selector*
:   A CSS simple selector.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Pseudo-Classes</span>

-   [:target pseudo-class selector](/CSS/Selectors/pseudo-classes/:target)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   **:required**

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

#### <span>Selectors</span>

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

-   [ID](/css/selectors/ID)

-   [Namespaced](/css/selectors/Namespaced)

-   [Universal](/css/selectors/Universal)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [whitespace](/css/selectors/attributes/whitespace)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   **:required**

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

-   [::selection](/w/index.php?title=selection&action=edit&redlink=1)

-   [type](/css/selectors/type)

### <span>Related pages (MSDN)</span>

-   `HTML5 Forms (Internet Explorer 10 Guide for Developers)`
-   `required attribute`
-   `Related pseudo-classes`
-   `:invalid`
-   `:optional`
-   `:valid`
