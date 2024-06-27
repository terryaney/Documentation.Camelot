# BTRGetERContribution Function

DOC: Han, Cfgena replacement?  Returns employer contributions.

## Syntax

```excel
=BTRGetERContribution(contributionType, contributionParam, year, monthEnd, payPeriod, rateOfPay, payPeriodWhenPayIncreases, rateOfPayIncrease, rateOfInflation, rateOfReturn, startPayPeriod, ytdPay, ytdErContribution, ageBOY, svcBOY, erContributionAnnualLimit, erContributionFrequency, midPointContribution, noLimit, limitPay, limitContribution, isOverflowToNonQual)
```

Parameter | Type | Description
---|---|---
`contributionType` | Int32 | Required.  The ContributionType to use for calculations.  PercentBasedOnAge = 1, PercentBasedOnService = 2, PercentBasedOnAgePlusService = 3.
`contributionParam` | String | Required.  Contribution parameters.  See matchParm for info.
`year` | Int32 | Required.  Calculation year.
`monthEnd` | Double | Required.  Calculate contributions as of the end of this month.
`payPeriod` | Int32 | Required.  Number of Pay period in a year.
`rateOfPay` | Double | Required.  Annual Pay rate as of start pay period.
`payPeriodWhenPayIncreases` | Int32 | Required.  Pay period when pay increases.
`rateOfPayIncrease` | Double | Required.  Pay increase rate.
`rateOfInflation` | Double | Required.  Inflation rate (used to project limits).
`rateOfReturn` | Double | Required.  Investment rate of return.
`startPayPeriod` | Object | Optional.  Starting Pay period.  Defaults to 1.
`ytdPay` | Double | Optional.  YTD savings pay.
`ytdErContribution` | Double | Optional.  YTD employer contributions.
`ageBOY` | Double | Optional.  Age at BOY.
`svcBOY` | Double | Optional.  Service at BOY.
`erContributionAnnualLimit` | Double | Optional.  Employer contribution annual limit. Defaults to unlimited.
`erContributionFrequency` | Int32 | Optional.  Frequency of ER Contribution in a year.
`midPointContribution` | Object | Optional.  Use mid point contributions timing calculation method.
`noLimit` | Object | Optional.  Don't apply IRS limit.
`limitPay` | Double | Optional.  Pay Limit.
`limitContribution` | Double | Optional.  Contribution limit.
`isOverflowToNonQual` | Boolean | Optional.  Overflow to non qualified plan.

[Back to Financial](RBLeFinancial.md)