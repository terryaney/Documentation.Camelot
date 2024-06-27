# BTRLogicAll Function

Returns 1 if all keys provided evaluate to not 'false' (#error, 0, FALSE) or 0 if any key provided is 'false'.  Each 'key' is a lookup into provided table, and the 'value' column is evalated for 'false'.

## Syntax

```excel
=BTRLogicAll(keys, table, valueColumn, caseSensitive)
```

Parameter | Type | Description
---|---|---
`keys` | String | Comma delimitted list of key values to use to find the rows in the table parameter.
`table` | Object[,] | Table containing the columns holding keys and values to find and do a falsy check (#error, 0, FALSE).
`valueColumn` | Object | The column (1..table columns) number containing the value to compare to ensure not falsy.  Default is the last column of 'table' parameter.
`caseSensitive` | Object | Whether or not a case sensitive search is performed. Default is false.

[Back to Validation](RBLeValidation.md)