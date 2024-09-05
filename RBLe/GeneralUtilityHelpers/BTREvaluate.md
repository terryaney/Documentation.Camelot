# BTREvaluate Function

Evaluates an Excel formula passed in.  If the formula contains one or more {K.id} tokens, each is parsed and the 'id' is used in BTRLookup to find a value to substitute into the formula

## Syntax

```excel
=BTREvaluate(formula, table, columnToReturn, columnToSearch, caseSensitive)
```

Parameter | Type | Default | Description
---|---|---|---
`formula` | String |  | Formula to evaluate with optional {K.id} tokens.
`table` | Object[,] |  | Range of cells to search (first row must be column headers).
`columnToReturn` | String? |  | Optional. Column name containing return value. Last column is default
`columnToSearch` | String? |  | Optional. Column name to search.  First column is default.
`caseSensitive` | Boolean? | `false` | Optional.  Whether or not search is case sensitive. false is the default.

[Back to General Utility Helpers](Readme.md) | [Back to All RBLe Functions](..\RBLe.md#function-documentation)