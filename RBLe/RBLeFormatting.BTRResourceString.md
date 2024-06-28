# BTRResourceString Function

Returns localized resource string.

## Syntax

```excel
=BTRResourceString(key, resourceStrings, culture, keyName)
```

Parameter | Type | Description
---|---|---
`key` | String | The resource key indicating which string to return.
`resourceStrings` | Object[,] | Range of cells to search.  The first row must be column headers with first column of key and additional columns for each culture or culture-subculture containing the values.
`culture` | String | Optional. The culture name to lookup.  If not provided, en-US is the default.
`keyName` | String | Optional. The name of the key column.  If not provided, 'key' is the default.

[Back to Formatting](RBLeFormatting.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)