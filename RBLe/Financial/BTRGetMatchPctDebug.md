# BTRGetMatchPctDebug Function

Debug version of BTRGetMatchPct that returns value or exception string (instead of #VALUE on error).  DOC: Han, Cfgena replacement?  Returns employer match % based on match parameters.

## Syntax

```excel
=BTRGetMatchPctDebug(matchType, isTrueUp, isMatchCatchUp, isPreTaxOverflowToAfterTax, isAfterTaxMatch, matchParam, year, monthEnd, payPeriod, rateOfPay, payPeriodWhenPayIncreases, rateOfPayIncrease, rateOfInflation, preTaxPercentage, preTaxFlatPerPayPeriod, rothPercentage, rothFlatPerPayPeriod, afterTaxPercentage, afterTaxFlatPerPayPeriod, startPayPeriod, ytdPay, ytdPreTax, ytdRoth, ytdAfterTax, ytdPreTaxCatchUp, ytdRothCatchUp, ytdErMatch, ageBOY, matchFrequency, limitAfterTax, isOverflowToCatchUp, preTaxCatchUpPercentage, preTaxCatchUpFlatPerPayPeriod, rothCatchUpPercentage, rothCatchUpFlatPerPayPeriod)
```

Parameter | Type | Default | Description
---|---|---|---
`matchType` | Int32 |  | Required.  The MatchType to use for calculations.  MultiplierBasedOnPercent = 1, ERMatchBasedOnPercent = 3
`isTrueUp` | Boolean |  | Required.  Whether to credit true-up math at the end of the year when employee hits contribution limit.
`isMatchCatchUp` | Boolean |  | Required.  Whether to provide match on catch-up contributions.
`isPreTaxOverflowToAfterTax` | Boolean |  | Required.  Whether to allow pre-tax contributions over limit to overflow to after-tax contributions.
`isAfterTaxMatch` | Boolean |  | Required.  Whether to provide match on after-tax contributions.
`matchParam` | String |  | Required.  \| delimited list of periods.  Each period is in the form of M:P:P where M is number of months for this period, and each P is a tier of a , seperated pair of decimal values.
`year` | Int32 |  | Required.  Calculation year.
`monthEnd` | Double |  | Required.  Calculate match as of the end of this month.
`payPeriod` | Int32 |  | Required.  Number of Pay period in a year.
`rateOfPay` | Double |  | Required.  Annual Pay rate as of start pay period.
`payPeriodWhenPayIncreases` | Int32 |  | Required.  Pay period when pay increases.
`rateOfPayIncrease` | Double |  | Required.  Pay increase rate.
`rateOfInflation` | Double |  | Required.  Inflation rate (used to project limits).
`preTaxPercentage` | Double? | `0` | Optional.  Pre-tax contribution as a % of pay.
`preTaxFlatPerPayPeriod` | Double? | `0` | Optional.  Flat $ pre-tax contribution amount per pay period.
`rothPercentage` | Double? | `0` | Optional.  Roth contribution as a % of pay.
`rothFlatPerPayPeriod` | Double? | `0` | Optional.  Flat $ Roth contribution amount per pay period.
`afterTaxPercentage` | Double? | `0` | Optional.  After-tax contribution as a % of pay.
`afterTaxFlatPerPayPeriod` | Double? | `0` | Optional.  Flat $ after-tax contribution amount per pay period.
`startPayPeriod` | Int32? | `1` | Optional.  Starting Pay period.  Defaults to 1.
`ytdPay` | Double? | `0` | Optional.  YTD savings pay.
`ytdPreTax` | Double? | `0` | Optional.  YTD pre-tax contributions.
`ytdRoth` | Double? | `0` | Optional.  YTD Roth contributions.
`ytdAfterTax` | Double? | `0` | Optional.  YTD after-tax contributions.
`ytdPreTaxCatchUp` | Double? | `0` | Optional.  YTD pre-tax catch-up contributions.
`ytdRothCatchUp` | Double? | `0` | Optional.  YTD Roth catch-up contributions.
`ytdErMatch` | Double? | `0` | Optional.  YTD employer match contributions.
`ageBOY` | Double? | `0` | Optional.  Age at BOY.
`matchFrequency` | Int32? | `0` | Optional.  Frequency of match in a year.
`limitAfterTax` | Double? | `0` | Optional.  Aftertax limit.
`isOverflowToCatchUp` | Boolean? | `true` | Optional.  Overflow from preTax to catchup.
`preTaxCatchUpPercentage` | Double? | `0` | Optional.  Pre-tax catchup contribution as a % of pay.
`preTaxCatchUpFlatPerPayPeriod` | Double? | `0` | Optional.  Flat $ pre-tax catchup contribution amount per pay period.
`rothCatchUpPercentage` | Double? | `0` | Optional.  Roth catchup contribution as a % of pay.
`rothCatchUpFlatPerPayPeriod` | Double? | `0` | Optional.  Flat $ Roth catchup contribution amount per pay period.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](..\RBLe.md#function-documentation)