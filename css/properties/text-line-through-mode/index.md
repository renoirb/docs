---
title: text-line-through-mode
notes:
  - 'Obsolete; deletion candidate'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`continuous`'
  'Applies to': 'all elements with and generated content with textual content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value (except for initial and inherit)'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`N/A`'
  Percentages: N/A
readiness: 'Not Ready'
summary: "Sets the mode for the line-through text decoration, determining whether the text decoration affects the space characters or not.\n"
tags:
  - CSS
  - Properties
uri: css/properties/text-line-through-mode

---
## <span>Summary</span>

Sets the mode for the line-through text decoration, determining whether the text decoration affects the space characters or not.

(Considered obsolete; use [text-decoration-skip](/css/properties/text-decoration-skip) instead.)

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `continuous`

Applies to
:   all elements with and generated content with textual content

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value (except for initial and inherit)

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `N/A`

Percentages
:   N/A

## <span>Syntax</span>

## <span>Values</span>

continuous
:   The line is continuous and covers white space.

skip-white-space
:   The line skips (does not include) white space characters.

## <span>Notes</span>

This property is obsolete and has been replaced by the [text-decoration-skip](/css/properties/text-decoration-skip) property.

Originally defined in an earlier draft of the [CSS3 Text Module specification](http://www.w3.org/TR/2003/CR-css3-text-20030514/), the functionality controlled by this property is now defined in the [CSS Text Decoration Level 3](http://www.w3.org/TR/css-text-decor-3) module. Sites (and apps) relying on the earlier behavior should be updated accordingly.