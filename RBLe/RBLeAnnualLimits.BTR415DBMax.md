# BTR415DBMax Function

A replacement function for the Cfgena.xla!AnnualLimits() function call with '415DBLimit' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum annual defined benefit payable at Social Security normal retirement age under §415(b).

## Syntax

```excel
=BTR415DBMax(year, rateProj)
```

Parameter | Type | Default | Description
---|---|---|---
`year` | Int32 |  | The effective year for the limit, if this parameter is 0 then function will return current year unrounded limit.
`rateProj` | Double |  | The increase rate at which to project the limit.

[Back to Annual Limits](RBLeAnnualLimits.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)