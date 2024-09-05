# BTRValidateAgeDate Function

Returns an integer indicating whether an input string is a valid age/date and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.

## Syntax

```excel
=BTRValidateAgeDate(value, dateBirth, minimum, maximum, dateOptions, culture, allowedFormats)
```

Parameter | Type | Default | Description
---|---|---|---
`value` | String |  | A string that contains a date or age to validate.
`dateBirth` | DateTime |  | The participant's date of birth.
`minimum` | DateTime |  | A DateTime representing the minimum value allowed if `value` is a date.
`maximum` | DateTime |  | A DateTime representing the minimum value allowed if `value` is a date.
`dateOptions` | DateOptionsType? | `DateOptionsType.None` | Additional options to apply to date (FirstOfMonthOrCoincident=1, LastOfMonthOrCoincident=2).
`culture` | String? | `"en-US"` | A string that supplies culture-specific format information about `value`.
`allowedFormats` | String? |  | A `\|` delimitted string that supplies a list of allowable formats to attempt to parse `value`.

[Back to Validation](Readme.md) | [Back to All RBLe Functions](/RBLe/RBLe.md#function-documentation)