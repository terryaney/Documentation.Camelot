# BTRPPASingleLife Function

Replacement function for the Cfgena.xla!PPASingleLife() function.  Returns a decimal value equal to the selected single life annuity factor by the PPA method.

## Remarks

If you defer a temporary or certain annuity to an age earlier than the individual's current age, the result is calculated only for the remainder of the annuity. For example, a 10-year temporary annuity deferred to age 65 for a 70-year old means that there are only 5 years remaining in the annuity and, thus, the result is equivalent to an immediate 5-year temporary annuity.
## Syntax

```excel
=BTRPPASingleLife(mortTable, intRate1, intRate2, intRate3, age, howDefer, whenDefer, howTemp, whenTemp, howCertain, whenCertain, pmtsPerYr, mortTableAdj, mortSizeAdj, mortImp, impEffYr, yob)
```

Parameter | Type | Default | Description
---|---|---|---
`mortTable` | String |  | Required.  The name of the mortality table that you wish to use.
`intRate1` | Double |  | Required.  The interest rate to use for years 0 - 4.
`intRate2` | Double |  | Required.  The interest rate to use for years 5 - 19.
`intRate3` | Double |  | Required.  The interest rate to use for years 20 and after.
`age` | Double |  | Required.  The current age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`howDefer` | String? | `"Y"` | The method used to determine deferrment age.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenDefer` | Double? | `0` | The age or years for deferred payment; 0-110.  When 'howDefer' is Y, deferred age is 'age' + value, otherwise value.  Default value is 0.
`howTemp` | String? | `"Y"` | The method used to determine temporary period.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenTemp` | Double? | `0` | The age or years for temporaryPeriod; 0-120.  When 'howTemp' is Y, temporary period age is 'age' + value, otherwise value.  Default value is 121, which means 'for life'.
`howCertain` | String? | `"Y"` | The method used to determine certain period.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenCertain` | Double? | `0` | The age or years for certain period; 0-110.  This has no effect prior to payment start time.  When 'howTemp' is A and 'whenTemp' is less than deferred age, certain period is 0, else when 'howCertain' is A, certain period is value - deferred age, otherwise value.  Default value is 0.
`pmtsPerYr` | Int32? | `12` | The frequency of payments per year (positive for beginning of period or negative for end of period payments).  Default value is 12.
`mortTableAdj` | Int32? | `0` | The adjustment years to apply as a shift to the mortality table (not the age). This is done before unisex blending.
`mortSizeAdj` | Double? | `1` | A multiplier to adjust the mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`mortImp` | Int32? | `0` | The 'MortalityImprovementType' to use, where 0 = Disable, 1 = DynamicScaleAA, 2 = StaticScaleAA, 31 = DynamicScaleBB, and 32 = StaticScaleBB.
`impEffYr` | Int32? | `-1` | The year of calculation if 'mortImp' is 1 or 2. The year entered in this argument will determine the effective year of the projected mortality table.
`yob` | Int32? | `0` | The year of birth for the member if dynamic generational is enabled 'mortImp' is 1.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)