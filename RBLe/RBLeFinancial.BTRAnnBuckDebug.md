# BTRAnnBuckDebug Function

A replacement function for the Annbuck.xla!AnnBuck() function.  Returns a decimal value representing the selected life annuity factor.

## Syntax

```excel
=BTRAnnBuckDebug(intRates, pmtTiming, age, spAge, sex, spSex, deferredAge, tempPeriod, guaranteePeriod, continuingPercentage, preRetirementMort, maleMortalityTable, femaleMortalityTable, maleUnisexPercentage, unisexBlending, maleTableAdjustment, femaleTableAdjustment, mortalityImprovement, improvementEffectiveYear, memberYearOfBirth, spouseYearOfBirth, dynamicImprovementStopYear, maleSizeAdjustment, femaleSizeAdjustment)
```

Parameter | Type | Description
---|---|---
`intRates` | Double[,] | Required.  A 6x2 array representing interest rates.  The first column refers to the period for which the corresponding interest rate in the second column applies.
`pmtTiming` | Int32 | Required.  The 'PaymentTimingType' to use where 1 = Continuous Approximation, 2 = Beginning of the month, and 3 = End of the month.
`age` | Double | Required.  The member's age to calculate; must be a decimal number between 0 and 120, inclusive.
`spAge` | Double | Required.  The spouse's age to calculate; must be a decimal number between 0 and 120, inclusive.  Use 0 when not calculating joint factors.
`sex` | Int32 | Required. The member's 'SexType' to use where 1 = Male and 2 = Female.
`spSex` | Int32 | Required. The spouse's 'SexType' to use where 1 = Male and 2 = Female.
`deferredAge` | Double | Required.  The age that benefits commence. For immediate factors, enter 0 or value equal to 'memberAge'.
`tempPeriod` | Double | Required.  The number of years that payments are made. Enter 0 if there is no temporary period.
`guaranteePeriod` | Double | Required.  The number of years for which payments are guaranteed upon death. Enter 0 if there is no guarantee period.
`continuingPercentage` | Double | Required.  The percentage that which payments will continue to the spouse upon death of the member.
`preRetirementMort` | Int32 | Required.  The 'PreRetirementMortalityType' to use, where 1 = NoMortality, 2 = MemberRetirementAgeJointSurvivor, 3 = MemberOnly, 4 = MemberDeathNoGuarantee, 5 = MemberRetirementAgeNoGuarantee, and 6 = MemberRetirementAgeFull.
`maleMortalityTable` | String | Required.  The number of the mortality table that you wish to use. For example, enter '214' for GAM83 Male.
`femaleMortalityTable` | String | Required.  The number of the mortality table that you wish to use.  See 'mMortTable'.
`maleUnisexPercentage` | Double | Required.  The unisex blending percentage applied to the male mortality table.
`unisexBlending` | Int32 | Required.  The 'UnisexBlendingType' to use, where 0 = Unisex off (sex distinct), 1 = Unisex blending by mortality rates, and 2 = Unisex blending by annuity factors.
`maleTableAdjustment` | Int32 | The adjustment years to apply as a shift to the male mortality table (not the age). This is done before unisex blending.
`femaleTableAdjustment` | Int32 | The adjustment years to apply as a shift to the female mortality table (not the age). This is done before unisex blending.
`mortalityImprovement` | Int32 | The 'MortalityImprovementType' to use, where 0 = Disable, 1 = DynamicScaleAA, 2 = StaticScaleAA, 11 = DynamicScaleCPMA1, 12 = StaticScaleCPMA1, 21 = DynamicScaleCPMA, 22 = StaticScaleCPMA, 31 = DynamicScaleBB, 32 = StaticScaleBB, 41 = DynamicScaleCPMB1, 42 = StaticScaleCPMB1, 51 = DynamicScaleCPMB, and 52 = StaticScaleCPMB.
`improvementEffectiveYear` | Object | The year of calculation if 'mortImp' is 1 or 2. The year entered in this argument will determine the effective year of the projected mortality table.
`memberYearOfBirth` | Int32 | The year of birth for the member if dynamic generational is enabled 'mortImp' is 1.
`spouseYearOfBirth` | Int32 | The year of birth for the spouse if dynamic generational is enabled 'mortImp' is 1.
`dynamicImprovementStopYear` | Object | The stop year if dynamic generational is enabled ('mortImp' is 1) and you wish to stop the generational projection at a future year. This caps the exponent of the projection factors. If this parameter is not filled in or a '0' then it is assumed that the improvements continue indefinitely.
`maleSizeAdjustment` | Object | A multiplier to adjust the male mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.
`femaleSizeAdjustment` | Object | A multiplier to adjust the female mortality rates (qx). Entering 0 or leaving it blank will multiply the rates by 1 (unchanged). Any other figure will serve as a multiplier. This action is done prior to applying unisex or generational improvements on the mortality table.

[Back to Financial](RBLeFinancial.md)