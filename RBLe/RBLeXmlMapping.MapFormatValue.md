# MapFormatValue Function

Returns 'value' formatted as string given the desired 'format' pattern.  Placeholder returning [FormatValue('value', 'format'] string.

## Syntax

```excel
=MapFormatValue(value, format, defaultValue)
```

Parameter | Type | Description
---|---|---
`value` | Object | The value (or model field) to format.
`format` | String | A valid C# format string in the format of {0:format}.
`defaultValue` | Object | Value to return to make coding specification formulas easier.

[Back to Xml Mapping](RBLeXmlMapping.md)