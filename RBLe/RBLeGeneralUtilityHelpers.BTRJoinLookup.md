# BTRJoinLookup Function

Concatenates all values (or fallback is not found) from columnToReturn column in a table range (including column headers), using the specified separator between elements.  Similar to VLOOKUP but always does exact match, uses column names instead of numbers (prevents issues when columns are inserted or removed), can search specified column instead of always the first, and provides ability to give a default.

## Syntax

```excel
=BTRJoinLookup(values, table, columnToReturn, columnToSearch, fallback, caseSensitive, separator)
```

Parameter | Type | Description
---|---|---
`values` | String | Comma delimitted list of values to search for.
`table` | Object[,] | Range of cells to search (first row must be column headers).
`columnToReturn` | Object | Optional. Column name containing return value. Last column is default
`columnToSearch` | Object | Optional. Column name to search.  First column is default.
`fallback` | Object | Optional.  Value to return if a match is not found.  #N/A is the default.
`caseSensitive` | Object | Optional.  Whether or not search is case sensitive. false is the default.
`separator` | Object | Optional. The string to use as a separator.  The separator is included in the return string only if values has more than one element. ', ' is the default.

[Back to General Utility Helpers](RBLeGeneralUtilityHelpers.md)