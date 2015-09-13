---
title: flex-wrap
code_samples:
  - 'http://gist.github.com/4740662'
  - 'http://gist.github.com/4740667'
  - 'http://gist.github.com/4740670'
notes:
  - 'Add description and compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`nowrap`'
  'Applies to': 'flex containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flexWrap`'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The flex-wrap property controls whether the flex container is single-line or multi-line, and the direction of the cross-axis, which determines the direction in which new lines are stacked.'
tags:
  - CSS
  - Properties
uri: css/properties/flex-wrap

---
## <span>Summary</span>

The flex-wrap property controls whether the flex container is single-line or multi-line, and the direction of the cross-axis, which determines the direction in which new lines are stacked.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `nowrap`

Applies to
:   flex containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `flexWrap`

## <span>Syntax</span>

-   `flex-wrap: nowrap`
-   `flex-wrap: wrap`
-   `flex-wrap: wrap-reverse`

## <span>Values</span>

nowrap
:   The flex container is single-line. The cross-start direction is equivalent to either the start or before/head direction of the current [writing mode](/css/properties/writing-mode), whichever is in the cross axis, and the cross-end direction is the opposite direction of cross-start.

wrap
:   The flex container is multi-line. The cross-start direction is equivalent to either the start or before/head direction of the current [writing mode](/css/properties/writing-mode), whichever is in the cross axis, and the cross-end direction is the opposite direction of cross-start.

wrap-reverse
:   Same as **wrap**, except the cross-start and cross-end directions are swapped.

## <span>Examples</span>

Displaying children in a non-wrapping row

``` css
.list {
  display: flex;
  flex-wrap: nowrap;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740662)

Displaying children in a row wrapping to the next line

``` css
.list {
  display: flex;
  flex-wrap: wrap;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740667)

Displaying children in a row wrapping to the previous line

``` css
.list {
  display: flex;
  flex-wrap: wrap-reverse;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740670)

## <span>Related specifications</span>

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#flex-wrap-property)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Flexbox</span>

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   [flex](/css/properties/flex)

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   **flex-wrap**

-   [justify-content](/css/properties/justify-content)
