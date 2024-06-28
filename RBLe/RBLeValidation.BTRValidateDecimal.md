# BTRValidateDecimal Function

Returns an integer indicating whether an input string is a valid decimal value and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.

## Syntax

```excel
=BTRValidateDecimal(value, minimum, maximum, culture, decimalPlaces)
```

Parameter | Type | Description
---|---|---
`value` | String | A string that contains a date and time to convert.
`minimum` | Double | A double representing the minimum value allowed if 'value' is a double.
`maximum` | Double | A double representing the minimum value allowed if 'value' is a double.
`culture` | Object | An string that supplies culture-specific format information about 'value'.
`decimalPlaces` | Object | An integer value representing the maximum number of decimal places allowed.

[Back to Validation](RBLeValidation.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)