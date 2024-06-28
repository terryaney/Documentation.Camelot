# BTRNumberFormat Function

Formats a numeric value to a string representation using the specified format and culture-specific format information.

## Remarks

The `BTRNumberFormat` method is similar to Excel's `Format()` function with the exception that `BTRNumberFormat` can dynamically format a number based on `culture` using the same `format` string.  
  
*See Also*  
[Standard Numeric Format Strings](http://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx)  
[Custom Numeric Format Strings](http://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx)
## Syntax

```excel
=BTRNumberFormat(value, format, culture)
```

Parameter | Type | Description
---|---|---
`value` | Double | The numeric value to apply formatting to.
`format` | String | The C# string format to apply.  View the function's help for more detail on possible values.
`culture` | Object | Optional.  The culture name in the format languagecode2-country/regioncode2 (default of `en-US`).  See 'National Language Support (NLS) API Reference' for available names.

[Back to Formatting](RBLeFormatting.md)