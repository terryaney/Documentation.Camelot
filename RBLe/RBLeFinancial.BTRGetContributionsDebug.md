# BTRGetContributionsDebug Function

DOC: Han, Cfgena replacement?  Returns 401k contributions/match.

## Syntax

```excel
=BTRGetContributionsDebug(matchType, isTrueUp, isCatchUpMatch, isPreTaxOverflowToAfterTax, isMatchAfterTax, matchParam, contributionType, contributionParam, year, monthEnd, payPeriod, rateOfPay, payPeriodWhenPayIncreases, ratePayIncrease, rateOfInflation, rateOfReturn, preTaxPercentage, preTaxFlatPerPayPeriod, rothPercentage, rothFlatPerPayPeriod, afterTaxPercentage, afterTaxFlatPerPayPeriod, startPayPeriod, ytdPay, ytdPreTax, ytdRoth, ytdAfterTax, ytdPreTaxCatchUp, ytdRothCatchUp, ytdErMatch, ytdErContribution, ageBOY, svcBOY, erContributionAnnualLimit, isRetirementYear, matchFrequency, erContributionFrequency, preTaxRothPayIsLimited, midPointContribution, noLimit, increaseMonth, increaseFrequency, increasePercentage, rateMax, limitPay, limitPreTax, limitContribution, isOverflowToNonQual, limitAfterTax, isOverflowToCatchUp, preTaxCatchUpPercentage, preTaxCatchUpFlatPerPayPeriod, rothCatchUpPercentage, rothCatchUpFlatPerPayPeriod, matchPayIsLimited)
```

Parameter | Type | Description
---|---|---
`matchType` | Int32 | Required.  The MatchType to use for calculations.  MultiplierBasedOnPercent = 1, MultiplierBasedOnDollars = 2, ERMatchPercentBasedOnPercent = 3, ERMatchDollarsBasedOnDollars = 4.
`isTrueUp` | Boolean | Required.  Whether to credit true-up math at the end of the year when employee hits contribution limit.
`isCatchUpMatch` | Boolean | Required.  Whether to provide match on catch-up contributions.
`isPreTaxOverflowToAfterTax` | Boolean | Required.  Whether to allow pre-tax contributions over limit to overflow to after-tax contributions.
`isMatchAfterTax` | Boolean | Required.  Whether to provide match on after-tax contributions.
`matchParam` | String | Required.  | delimited list of periods.  Each period is in the form of M:P:P where M is number of months for this period, and each P is a tier of a , seperated pair of decimal values.
`contributionType` | Int32 | Required.  The ContributionType to use for calculations.  PercentBasedOnAge = 1, PercentBasedOnService = 2, PercentBasedOnAgePlusService = 3.
`contributionParam` | String | Required.  Contribution parameters.  See mPm for info.
`year` | Int32 | Required.  Calculation year.
`monthEnd` | Double | Required.  Calculate contributions as of the end of this month.
`payPeriod` | Int32 | Required.  Number of Pay period in a year.
`rateOfPay` | Double | Required.  Annual Pay rate as of start pay period.
`payPeriodWhenPayIncreases` | Int32 | Required.  Pay period when pay increases.
`ratePayIncrease` | Double | Required.  Pay increase rate.
`rateOfInflation` | Double | Required.  Inflation rate (used to project limits).
`rateOfReturn` | Double | Required.  Investment rate of return.
`preTaxPercentage` | Double | Optional.  Pre-tax contribution as a % of pay.
`preTaxFlatPerPayPeriod` | Double | Optional.  Flat $ pre-tax contribution amount per pay period.
`rothPercentage` | Double | Optional.  Roth contribution as a % of pay.
`rothFlatPerPayPeriod` | Double | Optional.  Flat $ Roth contribution amount per pay period.
`afterTaxPercentage` | Double | Optional.  After-tax contribution as a % of pay.
`afterTaxFlatPerPayPeriod` | Double | Optional.  Flat $ after-tax contribution amount per pay period.
`startPayPeriod` | Object | Optional.  Starting Pay period.  Defaults to 1.
`ytdPay` | Double | Optional.  YTD savings pay.
`ytdPreTax` | Double | Optional.  YTD pre-tax contributions.
`ytdRoth` | Double | Optional.  YTD Roth contributions.
`ytdAfterTax` | Double | Optional.  YTD after-tax contributions.
`ytdPreTaxCatchUp` | Double | Optional.  YTD pre-tax catch-up contributions.
`ytdRothCatchUp` | Double | Optional.  YTD Roth catch-up contributions.
`ytdErMatch` | Double | Optional.  YTD employer match contributions.
`ytdErContribution` | Double | Optional.  YTD employer contributions.
`ageBOY` | Double | Optional.  Age at BOY.
`svcBOY` | Double | Optional.  Service at BOY.
`erContributionAnnualLimit` | Double | Optional.  Employer contribution annual limit. Defaults to 0, which means unlimited.
`isRetirementYear` | Boolean | Optional.  DOC: Han, Is this retirement year?
`matchFrequency` | Int32 | Optional.  Frequency of match in a year.
`erContributionFrequency` | Int32 | Optional.  Frequency of ER Contribution in a year.
`preTaxRothPayIsLimited` | Object | Optional.  Employee Pretax/Roth & Catchup Contributions is based on limited pay.
`midPointContribution` | Boolean | Optional.  Use mid point contributions timing calculation method.
`noLimit` | Boolean | Optional.  Don't apply IRS limit.
`increaseMonth` | Int32 | Optional.  Pretax auto increase timing (month): Enter 4 if increase happens on 4/1.
`increaseFrequency` | Int32 | Optional.  Pretax auto increase frequency per year.
`increasePercentage` | Double | Optional.  Pretax auto increase percentage.
`rateMax` | Double | Optional.  Pretax maximum rate.
`limitPay` | Double | Optional.  Pay Limit.
`limitPreTax` | Double | Optional.  Pretax limit.
`limitContribution` | Double | Optional.  Contribution limit.
`isOverflowToNonQual` | Boolean | Optional.  Overflow to non qualified plan.
`limitAfterTax` | Double | Optional.  Aftertax limit.
`isOverflowToCatchUp` | Object | Optional.  Overflow from preTax to catchup.
`preTaxCatchUpPercentage` | Double | Optional.  Pre-tax catchup contribution as a % of pay.
`preTaxCatchUpFlatPerPayPeriod` | Double | Optional.  Flat $ pre-tax catchup contribution amount per pay period.
`rothCatchUpPercentage` | Double | Optional.  Roth catchup contribution as a % of pay.
`rothCatchUpFlatPerPayPeriod` | Double | Optional.  Flat $ Roth catchup contribution amount per pay period.
`matchPayIsLimited` | Object | Optional.  Employer match is based on limited pay.

[Back to Financial](RBLeFinancial.md)