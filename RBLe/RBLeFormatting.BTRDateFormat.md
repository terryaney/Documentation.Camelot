# BTRDateFormat Function

Formats a Date value to a string representation using the specified format and culture-specific format information.

**Returns:** The string representation of the value of this instance as specified by `format` and `culture`.
## Remarks

The `BTRDateFormat` method is similar to Excel's `Format()` function with the exception that `BTRDateFormat` can dynamically format a date based on `culture` using the same `format` string.  
  
*See Also*  
[Standard Date and Time Format Strings](http://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)  
[Custom Date and Time Format Strings](http://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)
## Syntax

```excel
=BTRDateFormat(value, format, culture)
```

Parameter | Type | Description
---|---|---
`value` | Object | The date to apply a format to.
`format` | String | The C# string format to apply.  View the function's help for more detail on possible values.
`culture` | Object | Optional.  The culture name in the format languagecode2-country/regioncode2.  See 'National Language Support (NLS) API Reference' for available names.

[Back to Formatting](RBLeFormatting.md)