# BTRHCELimit Function

A replacement function for the Cfgena.xla!AnnualLimits() function call with 'HCECompLimit' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing annual compensation used to define highly compensated employee after 1996.

## Syntax

```excel
=BTRHCELimit(year, rateProj)
```

Parameter | Type | Description
---|---|---
`year` | Int32 | The effective year for the limit, if this parameter is 0 then function will return current year unrounded limit.
`rateProj` | Double | The increase rate at which to project the limit.

[Back to Annual Limits](RBLeAnnualLimits.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)