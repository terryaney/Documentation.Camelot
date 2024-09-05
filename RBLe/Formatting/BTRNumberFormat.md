# BTRNumberFormat Function

Formats a numeric value to a string representation using the specified format and culture-specific format information.

**Returns:** The string representation of the value of this instance as specified by `format` and `culture`.
## Remarks

The `BTRNumberFormat` method is similar to Excel's `Format()` function with the exception that `BTRNumberFormat` can dynamically format a number based on `culture` using the same `format` string.  
  
*See Also*  
[Standard Numeric Format Strings](http://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx)  
[Custom Numeric Format Strings](http://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx)
## Syntax

```excel
=BTRNumberFormat(value, format, culture)
```

Parameter | Type | Default | Description
---|---|---|---
`value` | Double |  | The numeric value to apply formatting to.
`format` | String |  | The C# string format to apply.  View the function's help for more detail on possible values.
`culture` | String? | `"en-US"` | Optional.  The culture name in the format languagecode2-country/regioncode2 (default of `en-US`).  See 'National Language Support (NLS) API Reference' for available names.

## Example

This sample shows how to format a numeric value to currency format with a single format string but changes based on culture.

```
// Assume this comes from the iCurrentCulture input.
string culture = "en-US";
// Assume this comes from a calculated result.
double value = 10.5;
// currencyValue would have "$10.50" for a value.
string currencyValue = BTRNumberFormat( value, "c", culture );
// If culture was French...
culture = "fr-FR";
// currencyValue would have "10,50 €" for a value.
currencyValue = BTRNumberFormat( value, "c", culture );
```
[Back to Formatting](Readme.md) | [Back to All RBLe Functions](..\RBLe.md#function-documentation)