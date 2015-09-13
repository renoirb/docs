---
title: grid-auto-columns
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'As specified'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Changes default size of columns.  Creates implicit grid tracks when a grid item is placed into a row or column that is not explicitly sized (by grid-template-rows or grid-template-columns).  This property (with grid-auto-rows) specifies the default size of such implicitly-created tracks.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-auto-columns

---
## <span>Summary</span>

Changes default size of columns. Creates implicit grid tracks when a grid item is placed into a row or column that is not explicitly sized (by grid-template-rows or grid-template-columns). This property (with grid-auto-rows) specifies the default size of such implicitly-created tracks.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Grid containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   As specified

## <span>Syntax</span>

-   `grid-auto-columns: <track-size>`

## <span>Values</span>

\<track-size\>
:   A space-separated track list specifying the line names and track sizing functions of the grid. See [track sizing](http://www.w3.org/TR/css3-grid-layout/#track-sizing) in specification for details.

## <span>Examples</span>

``` css
/*
Grid item B is positioned in column 5.  This automatically generates four implicit columns (1-4) and one implicit row (2).
The implicit (auto) columns and rows are sized at 20px
using grid-auto-columns and grid-column-rows.
*/
<style type="text/css">
  #grid {
display: grid;
grid-auto-columns: 20px;
grid-auto-rows: 20px }
  #A { grid-column: 1;          grid-row: 1; }
  #B { grid-column: 5;          grid-row: 1 / span 2; }
  #C { grid-column: 1 / span 2; grid-row: 2; }
</style>
```

## <span>Related specifications</span>

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
