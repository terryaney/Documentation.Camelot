# BTRGetERContributionPctDebug Function

Debug version of BTRGetERContributionPct that returns value or exception string (instead of #VALUE on error).  DOC: Han, Cfgena replacement?  Returns employer contribution % based on contribution parameters.

## Syntax

```excel
=BTRGetERContributionPctDebug(contributionType, contributionParam, year, monthEnd, payPeriod, rateOfPay, payPeriodWhenPayIncreases, rateOfPayIncrease, rateOfInflation, startPayPeriod, ytdPay, ytdErContribution, ageBOY, svcBOY, erContributionAnnualLimit, erContributionFrequency)
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
`startPayPeriod` | Int32 | Optional.  Starting pay period.  Defaults to 1.
`ytdPay` | Double | Optional.  YTD savings pay.
`ytdErContribution` | Double | Optional.  YTD employer contributions.
`ageBOY` | Double | Optional.  Age at BOY.
`svcBOY` | Double | Optional.  Service at BOY.
`erContributionAnnualLimit` | Double | Optional.  Employer contribution annual limit. Defaults to unlimited.
`erContributionFrequency` | Int32 | Optional.  Frequency of ER Contribution in a year.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)