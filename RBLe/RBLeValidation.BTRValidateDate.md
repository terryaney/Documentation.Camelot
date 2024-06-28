# BTRValidateDate Function

Returns an integer indicating whether an input string is a valid date and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.

## Syntax

```excel
=BTRValidateDate(value, minimum, maximum, culture, allowedFormats, validDates)
```

Parameter | Type | Default | Description
---|---|---|---
`value` | String |  | A string that contains a date and time to convert.
`minimum` | DateTime |  | A DateTime representing the minimum value allowed if 'value' is a date.
`maximum` | DateTime |  | A DateTime representing the minimum value allowed if 'value' is a date.
`culture` | String? | `"en-US"` | A string that supplies culture-specific format information about 'value'.
`allowedFormats` | String? |  | A \| delimitted string that supplies a list of allowable formats to attempt to parse 'value'.
`validDates` | String? |  | A , delimitted string of allowable dates to validate in the format of 1..N, Last, Mon-Sun, Mon-Sun.[N\|Last] (Nth occurence of or last day in month), or W1-W5 (first through the fifth week of month).  If the 'pattern' starts with '!' it is a 'not' check.

[Back to Validation](RBLeValidation.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)