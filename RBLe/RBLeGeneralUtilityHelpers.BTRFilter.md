# BTRFilter Function

Returns a filtered table given a list of filter columns and values to compare.

## Syntax

```excel
=BTRFilter(table, returnColumns, includeHeadersInResults, expressions)
```

Parameter | Type | Description
---|---|---
`table` | Object[,] | Range of cells to filter.
`returnColumns` | String | Comma delimitted list of column names that should be included in returned range.
`includeHeadersInResults` | Boolean | Optional.  Whether or not to include column headers in result table. Default is true.
`expressions` | Object[] | Paired expressions.  First item is column name to search, second item is value to filter.

[Back to General Utility Helpers](RBLeGeneralUtilityHelpers.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)