---
title: flex-direction
code_samples:
  - 'http://gist.github.com/4740224'
  - 'http://gist.github.com/4740260'
  - 'http://gist.github.com/4740271'
  - 'http://gist.github.com/4740277'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`row`'
  'Applies to': 'flex containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flexDirection`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The flex-direction CSS property describes how flex items are placed in the flex container, by setting the direction of the flex container''s main axis.'
tags:
  0: CSS
  1: Properties
  3: Flexbox
uri: css/properties/flex-direction

---
## <span>Summary</span>

The flex-direction CSS property describes how flex items are placed in the flex container, by setting the direction of the flex container's main axis.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `row`

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
:   `flexDirection`

## <span>Syntax</span>

-   `flex-direction: column`
-   `flex-direction: column-reverse`
-   `flex-direction: row`
-   `flex-direction: row-reverse`

## <span>Values</span>

row
:   The flex container's main axis has the same orientation as the inline axis of the current [writing mode](/css/properties/writing-mode). The main-start and main-end directions are equivalent to the start and end directions, respectively, of the current [writing mode](/css/properties/writing-mode).

row-reverse
:   Same as 'row', except the main-start and main-end directions are swapped.

column
:   The flex container's main axis has the same orientation as the block axis of the current [writing mode](/css/properties/writing-mode). The main-start and main-end directions are equivalent to the before/head and after/foot directions, respectively, of the current [writing mode](/css/properties/writing-mode).

column-reverse
:   Same as 'column', except the main-start and main-end directions are swapped.

## <span>Examples</span>

Displaying children in a row

``` css
.list {
  display: flex;
  flex-direction: row;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740224)

Displaying children in a row in reversed order

``` css
.list {
  display: flex;
  flex-direction: row-reverse;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740260)

Displaying children in a column

``` css
.list {
  display: flex;
  flex-direction: column;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740271)

Displaying children in a column in reversed order

``` css
.list {
  display: flex;
  flex-direction: column-reverse;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740277)

## <span>Notes</span>

The reverse values do not reverse box ordering; like ‘writing-mode’ and ‘direction’, they only change the direction of flow. Painting order, speech order, and sequential navigation orders are not affected.

## <span>Related specifications</span>

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#flex-direction-property)
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

-   **flex-direction**

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)
