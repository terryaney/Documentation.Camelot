# BTRSingleLifeComm Function

Replacement function for the Cfgena.xla!SingleLife() function.  Returns a decimal value equal to the selected single life annuity factor.

## Syntax

```excel
=BTRSingleLifeComm(mortTable, intRate, age, typeCF, pmtsPerYear, mortTableAdj, mortSizeAdj, mortalityImprovement, improvementEffectiveYear, memberYearOfBirth, dynamicImprovementStopYear)
```

Parameter | Type | Default | Description
---|---|---|---
`mortTable` | String |  | Required.  The name of the mortality table that you wish to use.
`intRate` | Double |  | Required.  The interest rate to use.
`age` | Double |  | Required.  The current age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`typeCF` | String? | `""` | Commutation Function (CF) type, please see CFGENA help for details.
`pmtsPerYear` | Int32? | `12` | The frequency of payments per year (positive for beginning of period or negative for end of period payments).  Default value is 12.
`mortTableAdj` | Int32? | `0` | The adjustment years to apply as a shift to the mortality table (not the age). This is done before unisex blending.
`mortSizeAdj` | Double? | `1` | A multiplier to adjust the mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`mortalityImprovement` | Int32? | `0` | The 'MortalityImprovementType' to use, where 0 = Disable, 1 = DynamicScaleAA, 2 = StaticScaleAA, 31 = DynamicScaleBB, and 32 = StaticScaleBB.
`improvementEffectiveYear` | Int32? | `-1` | The year of calculation if 'mortImp' is 1 or 2. The year entered in this argument will determine the effective year of the projected mortality table.
`memberYearOfBirth` | Int32? | `0` | The year of birth for the member if dynamic generational is enabled 'mortImp' is 1.
`dynamicImprovementStopYear` | Int32? | `9999` | The stop year if dynamic generational is enabled ('mortImp' is 1) and you wish to stop the generational projection at a future year. This caps the exponent of the projection factors. If this parameter is not filled in or a '0' then it is assumed that the improvements continue indefinitely.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)