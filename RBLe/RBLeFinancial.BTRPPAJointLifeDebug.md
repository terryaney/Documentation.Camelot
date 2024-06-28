# BTRPPAJointLifeDebug Function

Replacement function for the Cfgena.xla!PPAJointLife() function.  Returns a decimal value equal to the selected joint life annuity factor by the PPA method.

## Syntax

```excel
=BTRPPAJointLifeDebug(mortTable, spMortTable, intRate1, intRate2, intRate3, age, spAge, annuityOption, jointFraction, howDefer, whenDefer, howTemp, whenTemp, howCertain, whenCertain, pmtsPerYr, maleTableAdjustment, femailTableAdjustment, maleSizeAdjustment, femaleSizeAdjustment, maleUnisexPercentage, unisexBlending, mortImp, improvementEffectiveYear, memberYearOfBirth, spouseYearOfBirth, dynamicImprovementStopYear)
```

Parameter | Type | Description
---|---|---
`mortTable` | String | Required.  The name of the mortality table that you wish to use.
`spMortTable` | String | Required.  The name of the mortality table that you wish to use.
`intRate1` | Double | Required.  The interest rate to use for years 0 - 4.
`intRate2` | Double | Required.  The interest rate to use for years 5 - 19.
`intRate3` | Double | Required.  The interest rate to use for years 20 and after.
`age` | Double | Required.  The current member age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`spAge` | Double | Required.  The spouse age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`annuityOption` | Object | The options for annuity factors. 'C' for contingent, 'S' for survivor, 'P' for popup, 'D' for double popup and 'J' for joint life factor only.  Default value is 'C'.
`jointFraction` | Object | The fraction of contingent/survivor amount to the primary amount; 0-1.  Default value is 0.5.
`howDefer` | Object | The method used to determine deferrment age.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenDefer` | Double | The age or years for deferred payment; 0-110.  When 'howDefer' is Y, deferred age is 'age' + value, otherwise value.  Default value is 0.
`howTemp` | Object | The method used to determine temporary period.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenTemp` | Double | The age or years for temporaryPeriod; 0-120.  When 'howTemp' is Y, temporary period age is 'age' + value, otherwise value.  Default value is 121, which means 'for life'.
`howCertain` | Object | The method used to determine certain period.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenCertain` | Double | The age or years for certain period; 0-110.  This has no effect prior to payment start time.  When 'howTemp' is A and 'whenTemp' is less than deferred age, certain period is 0, else when 'howCertain' is A, certain period is value - deferred age, otherwise value.  Default value is 0.
`pmtsPerYr` | Object | The frequency of payments per year (positive for beginning of period or negative for end of period payments).  Default value is 12.
`maleTableAdjustment` | Int32 | The adjustment years to apply as a shift to the male mortality table (not the age). This is done before unisex blending.
`femailTableAdjustment` | Int32 | The adjustment years to apply as a shift to the female mortality table (not the age). This is done before unisex blending.
`maleSizeAdjustment` | Object | A multiplier to adjust the male mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`femaleSizeAdjustment` | Object | A multiplier to adjust the female mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`maleUnisexPercentage` | Object | The unisex blending percentage applied to the male mortality table.
`unisexBlending` | Int32 | The 'UnisexBlendingType' to use, where 0 = Unisex off (sex distinct), 1 = Unisex blending by mortality rates, and 2 = Unisex blending by annuity factors.
`mortImp` | Int32 | The 'MortalityImprovementType' to use, where 0 = Disable, 1 = DynamicScaleAA, 2 = StaticScaleAA, 31 = DynamicScaleBB, and 32 = StaticScaleBB.
`improvementEffectiveYear` | Object | The year of calculation if 'mortImp' is 1 or 2. The year entered in this argument will determine the effective year of the projected mortality table.
`memberYearOfBirth` | Int32 | The year of birth for the member if dynamic generational is enabled 'mortImp' is 1.
`spouseYearOfBirth` | Int32 | The year of birth for the spouse if dynamic generational is enabled 'mortImp' is 1.
`dynamicImprovementStopYear` | Object | The stop year if dynamic generational is enabled ('mortImp' is 1) and you wish to stop the generational projection at a future year. This caps the exponent of the projection factors. If this parameter is not filled in or a '0' then it is assumed that the improvements continue indefinitely.

[Back to Financial](RBLeFinancial.md)