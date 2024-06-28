# BTRParseAgeDate Function

Validates and converts the input string representation of an age/date, supporting culture specific formats, to its Date equivalent.  Throws an exception if not a valid age/date.

## Syntax

```excel
=BTRParseAgeDate(value, dateBirth, dateOptions, culture, allowedFormats)
```

Parameter | Type | Description
---|---|---
`value` | String | A string that contains a date or age to convert.
`dateBirth` | DateTime | The participant's date of birth.
`dateOptions` | Object | Additional options to apply to date (FirstOfMonthOrCoincident=1, LastOfMonthOrCoincident=2).
`culture` | Object | An string that supplies culture-specific format information about 'value'.
`allowedFormats` | String | An | delimitted string that supplies a list of allowable formats to attempt to parse 'value'.

[Back to Validation](RBLeValidation.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)