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

Parameter | Type | Default | Description
---|---|---|---
`value` | Object | `` | The date to apply a format to.
`format` | String | `""` | The C# string format to apply.  View the function's help for more detail on possible values.
`culture` | String? | `"en-US"` | Optional.  The culture name in the format languagecode2-country/regioncode2 (default of `en-US`).  See 'National Language Support (NLS) API Reference' for available names.

## Example

This sample shows how to format a date value to 'short date' format with a single format string but changes based on culture.

```
// Assume this comes from the iCurrentCulture input.
string culture = "en-US";
// Assume this comes from a calculated result.
DateTime value = new DateTime( 1973, 5, 9 );
// dateValue would have "5/9/1973" for a value.
string dateValue = BTRDateFormat( value, "d", culture );
// If culture was French...
culture = "fr-FR";
// dateValue would have "09/05/1973" for a value.
dateValue = BTRDateFormat( value, "d", culture );
```
[Back to Formatting](RBLeFormatting.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)