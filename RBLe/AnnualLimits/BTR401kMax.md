# BTR401kMax Function

A replacement function for the Cfgena.xla!AnnualLimits() function call with 'Max401(k)Contribution' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum permitted salary deferral under §401(k).

## Syntax

```excel
=BTR401kMax(year, rateProj)
```

Parameter | Type | Default | Description
---|---|---|---
`year` | Int32 |  | The effective year for the limit, if this parameter is 0 then function will return current year unrounded limit.
`rateProj` | Double |  | The increase rate at which to project the limit.

[Back to Annual Limits](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)