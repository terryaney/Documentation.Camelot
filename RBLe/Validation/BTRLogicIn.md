# BTRLogicIn Function

Returns 1 if 'value' is present anywhere in the 'table' parameter.

## Syntax

```excel
=BTRLogicIn(value, table, caseSensitive, delimitter)
```

Parameter | Type | Default | Description
---|---|---|---
`value` | Object |  | The value to search for.
`table` | Object[,] |  | Table containing values to search.
`caseSensitive` | Boolean? | `false` | Whether or not a case sensitive search is performed. Default is false.
`delimitter` | Char? | `null` | An optional delimitter character to split items in 'table' before performing the compare.  Default is null.

[Back to Validation](RBLeValidation.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)