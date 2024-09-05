# BTRCellAddress Function

Returns the address (similar to Cell('address', cell) format) of a named range to be used in RBLe Macro processing.

## Syntax

```excel
=BTRCellAddress(range, rowOffset, columnOffset, additionalRows, additionalColumns)
```

Parameter | Type | Default | Description
---|---|---|---
`range` | Object |  | The cell or range used as starting point of address.
`rowOffset` | Int32? | `0` | The number of rows (positive, negative, or 0 (zero)) by which the range is to be offset. Positive values are offset downward, and negative values are offset upward. The default value is 0.
`columnOffset` | Int32? | `0` | The number of columns (positive, negative, or 0 (zero)) by which the range is to be offset. Positive values are offset to the right, and negative values are offset to the left. The default value is 0.
`additionalRows` | Int32? | `0` | The number of rows (positive, negative, or 0 (zero)) by which the range is to be resized. Positive values grow downward, and negative values shrink upward. The default value is 0.
`additionalColumns` | Int32? | `0` | The number of columns (positive, negative, or 0 (zero)) by which the range is to be resized. Positive values grow to the right, and negative values shrink to the left. The default value is 0.

[Back to RBLe Macro](RBLeRBLeMacro.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)