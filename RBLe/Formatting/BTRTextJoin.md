# BTRTextJoin Function

Concatenates a list or range of text strings using a delimiter. Polyfill for non-supported Excel TEXTJOIN function.

## Syntax

```excel
=BTRTextJoin(seperator, ignoreEmptyCells, ranges)
```

Parameter | Type | Default | Description
---|---|---|---
`seperator` | Object? |  | Optional. The separator to use between values. Default is empty string.
`ignoreEmptyCells` | Boolean? | `true` | Optional. Whether or not to ignore empty cells.  Default is true
`ranges` | Object[] |  | 1 to 252 text strings or ranges to be joined.

[Back to Formatting](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)