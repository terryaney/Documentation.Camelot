# BTRJointLife Function

Replacement function for the Cfgena.xla!JointLife() function.  Returns decimal value equal to the selected joint life annuity factor.

## Remarks

If you defer a temporary or certain annuity to an age earlier than the individual's current age, the result is calculated only for the remainder of the annuity. For example, a 10-year temporary annuity deferred to age 65 for a 70-year old means that there are only 5 years remaining in the annuity and, thus, the result is equivalent to an immediate 5-year temporary annuity.  
Non-integer values for `memberAge`, `spouseAge`, `deferredAge`, `temporaryPeriod`, and `guaranteePeriod` can be used.  The factor will then be interpolated.  
An `ArgumentOutOfRangeException` can be thrown if any of the following conditions occur:  
1. `intRates` durations contain any negative or decimal numbers or the sum of the durations greater than 120.  
2. `memberAge` is less than 1 or greater than 120.  
3. `spouseAge` is less than 1 or greater than 120.  
4. `deferredAge` is less than 0 or greater than 120 or less than `memberAge` (when `deferredAge` > 0).  
5. `mortalityImprovement` is not 0, 1, 2, 31 or 32.  
6. `mortalityImprovement` is 1 or 31 and `unisexBlending` is 2 or `memberYearOfBirth` is 0 or `spouseYearOfBirth` is 0.  
7. `continuingPercentage` is less than 0.  
8. `maleUnisexPercentage` is less than 0 or greater than 1.  
9. `unisexBlending` is not 0, 1, or 2  
10. `temporaryPeriod` is less than 0 or greater than Min( 120 - Max( `memberAge`, `spouseAge` ), 120 - `deferredAge` ).  
11. `guaranteePeriod` is greater than `temporaryPeriod` (when `temporaryPeriod` is greater than 0).  
12. `maleTableAdjustment` or `femaleTableAdjustment` is less than Max( -10, `-age` ) or greater than Min( 10, 120 - `age` ).
## Syntax

```excel
=BTRJointLife(mortTable, spMortTable, intRate, age, spAge, annuityOption, jointFraction, howDefer, whenDefer, howTemp, whenTemp, howCertain, whenCertain, pmtsPerYr, maleTableAdjustment, femaleTableAdjustment, maleSizeAdjustment, femaleSizeAdjustment, maleUnisexPercentage, unisexBlending, mortalityImprovement, improvementEffectiveYear, memberYearOfBirth, spouseYearOfBirth, dynamicImprovementStopYear)
```

Parameter | Type | Description
---|---|---
`mortTable` | String | Required.  The name of the mortality table that you wish to use.
`spMortTable` | String | Required.  The name of the mortality table that you wish to use.
`intRate` | Double | Required.  The interest rate to use.
`age` | Double | Required.  The current member age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`spAge` | Double | Required.  The current spouse age (see Remarks) to calculate the factor of. Value is typically 20 to 110 (matching mortality table ages). Interpolation is performed if value is not integral.
`annuityOption` | String | The options for annuity factors. 'C' for contingent, 'S' for survivor, 'P' for popup, 'D' for double popup and 'J' for joint life factor only.  Default value is 'C'.
`jointFraction` | Double | The fraction of contingent/survivor amount to the primary amount; 0-1.  Default value is 0.5.
`howDefer` | String | The method used to determine deferrment age.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenDefer` | Double | The age or years for deferred payment; 0-110.  When 'howDefer' is Y, deferred age is 'age' + value, otherwise value.  Default value is 0.
`howTemp` | String | The method used to determine temporary period.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenTemp` | Double | The age or years for temporaryPeriod; 0-120.  When 'howTemp' is Y, temporary period age is 'age' + value, otherwise value.  Default value is 121, which means 'for life'.
`howCertain` | String | The method used to determine certain period.  'A' for age, 'Y' for years.  Default value is 'Y'.
`whenCertain` | Double | The age or years for certain period; 0-110.  This has no effect prior to payment start time.  When 'howTemp' is A and 'whenTemp' is less than deferred age, certain period is 0, else when 'howCertain' is A, certain period is value - deferred age, otherwise value.  Default value is 0.
`pmtsPerYr` | Int32 | The frequency of payments per year (positive for beginning of period or negative for end of period payments).  Default value is 12.
`maleTableAdjustment` | Int32 | The adjustment years to apply as a shift to the male mortality table (not the age). This is done before unisex blending.
`femaleTableAdjustment` | Int32 | The adjustment years to apply as a shift to the female mortality table (not the age). This is done before unisex blending.
`maleSizeAdjustment` | Double | A multiplier to adjust the male mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`femaleSizeAdjustment` | Double | A multiplier to adjust the female mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`maleUnisexPercentage` | Double | The unisex blending percentage applied to the male mortality table.
`unisexBlending` | Int32 | The 'UnisexBlendingType' to use, where 0 = Unisex off (sex distinct), 1 = Unisex blending by mortality rates, and 2 = Unisex blending by annuity factors.
`mortalityImprovement` | Int32 | The 'MortalityImprovementType' to use, where 0 = Disable, 1 = DynamicScaleAA, 2 = StaticScaleAA, 31 = DynamicScaleBB, and 32 = StaticScaleBB.
`improvementEffectiveYear` | Int32 | The year of calculation if 'mortImp' is 1 or 2. The year entered in this argument will determine the effective year of the projected mortality table.
`memberYearOfBirth` | Int32 | The year of birth for the member if dynamic generational is enabled 'mortImp' is 1.
`spouseYearOfBirth` | Int32 | The year of birth for the spouse if dynamic generational is enabled 'mortImp' is 1.
`dynamicImprovementStopYear` | Int32 | The stop year if dynamic generational is enabled ('mortImp' is 1) and you wish to stop the generational projection at a future year. This caps the exponent of the projection factors. If this parameter is not filled in or a '0' then it is assumed that the improvements continue indefinitely.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)