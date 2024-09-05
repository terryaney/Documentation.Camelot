# BTRValidateInteger Function

Returns an integer indicating whether an input string is a valid integer and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.

## Syntax

```excel
=BTRValidateInteger(value, minimum, maximum, culture)
```

Parameter | Type | Default | Description
---|---|---|---
`value` | String |  | A string that contains a date and time to convert.
`minimum` | Int32 |  | A integer representing the minimum value allowed if `value` is a integer.
`maximum` | Int32 |  | A integer representing the minimum value allowed if `value` is a integer.
`culture` | String? | `"en-US"` | A string that supplies culture-specific format information about `value`.

[Back to Validation](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)