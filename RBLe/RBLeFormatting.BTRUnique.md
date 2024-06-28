# BTRUnique Function

Returns a list of unique values from a given input range.

## Syntax

```excel
=BTRUnique(values, matchInputOutputSize, ignoreEmptyCells, ranges)
```

Parameter | Type | Description
---|---|---
`values` | Object[,] | Range of cells to find unique values contained.
`matchInputOutputSize` | Boolean | Optional. Whether or not to match size of `values` or the output from unique list when returning an array.  Default is true
`ignoreEmptyCells` | Boolean | Optional. Whether or not to ignore empty cells.  Default is true
`ranges` | Object[] | 1 to 252 ranges to merge.

[Back to Formatting](RBLeFormatting.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)