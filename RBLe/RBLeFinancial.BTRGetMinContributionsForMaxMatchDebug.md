# BTRGetMinContributionsForMaxMatchDebug Function

Debug version of BTRGetMinContributionsForMaxMatch that returns value or exception string (instead of #VALUE on error).  DOC: Han, Cfgena replacement?  Returns minimum employee contribution to get max mactch based on match parameters.

## Syntax

```excel
=BTRGetMinContributionsForMaxMatchDebug(matchType, matchParam, payPeriod, currPayPeriod)
```

Parameter | Type | Description
---|---|---
`matchType` | Int32 | Required.  The MatchType to use for calculations.  MultiplierBasedOnPercent = 1, ERMatchBasedOnPercent = 3
`matchParam` | String | Required.  | delimited list of periods.  Each period is in the form of M:P:P where M is number of months for this period, and each P is a tier of a , seperated pair of decimal values.
`payPeriod` | Object | Optional.  Number of Pay period in a year.  Default is 1.
`currPayPeriod` | Object | Optional.  Current Pay Period.  Default is 1.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)