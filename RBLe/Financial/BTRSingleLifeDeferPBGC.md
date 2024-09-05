# BTRSingleLifeDeferPBGC Function

Replacement function for the Cfgena.xla!SingleLifeDeferPBGC() function.  Returns a decimal value equal to the selected single life annuity factor.

## Syntax

```excel
=BTRSingleLifeDeferPBGC(mortTable, intRate, age, howDefer, whenDefer, intRate7, intRate8, intRateR, pmtsPerYear, mortTableAdj)
```

Parameter | Type | Default | Description
---|---|---|---
`mortTable` | String |  | Required.  The name of the mortality table that you wish to use.
`intRate` | Double |  | Required.  The interest rate to use.
`age` | Double |  | Required.  The current age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`howDefer` | String? | `"Y"` | The method used to determine deferrment age.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenDefer` | Double? | `0` | The age or years for deferred payment; 0-110.  When 'howDefer' is Y, deferred age is 'age' + value, otherwise value.  Default value is 0.
`intRate7` | Double? | `0.04` | Interest for first 7 deferral years, 0.06 is 6%. (Not allowed to be less than 4%.)
`intRate8` | Double? | `0.04` | Interest for next 8 deferral years, 0.05 is 5%. (Not allowed to be less than 4%.)
`intRateR` | Double? | `0.04` | Interest for remaining deferral years, 0.04 is 4%. (Not allowed to be less than 4%.)
`pmtsPerYear` | Int32? | `12` | The frequency of payments per year (positive for beginning of period or negative for end of period payments).  Default value is 12.
`mortTableAdj` | Int32? | `0` | The adjustment years to apply as a shift to the mortality table (not the age). This is done before unisex blending.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)