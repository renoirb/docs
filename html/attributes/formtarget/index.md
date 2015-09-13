---
title: formtarget
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies a name or a keyword that indicates where to display the response that is received after submitting the form.'
tags:
  - Markup
  - Attributes
uri: html/attributes/formtarget

---
## <span>Summary</span>

Specifies a name or a keyword that indicates where to display the response that is received after submitting the form.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLInputElement](/html/elements/input)

</td>
</tr>
</table>
The formtarget attribute overrides the target attribute of the \<form\> element.

## <span>Examples</span>

``` html
<form action="submit.php">
  Input field: <input type="text" name="inputfield">
  <input type="submit" value="Submit">
  <input type="submit" formtarget="_blank" value="Submit to a new window">
</form>
```

## <span>Related specifications</span>

[HTML5 Forms](http://www.w3.org/TR/html5/forms.html)
:   W3C Recommendation

