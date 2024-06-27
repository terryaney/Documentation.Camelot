# BTR401A17Max function

A replacement function for the Cfgena.xla!AnnualLimits() function call with '401(a)(17)PayLimit' name parameter in favor of explicit function name (reduces parameter typo errors). Returns an integer value representing maximum compensation recognized under qualified pension or profit sharing plans (ignores EGTRRA limit changes). Post-2001 limits are updated each year with the annual CPI/W rate.

## Syntax

```excel
=BTR401A17Max(year, rateProjection)
```

Parameter | Type | Description
---|---|---
`year` | int | The effective year for the limit, if this parameter is 0 then function will return current year unrounded limit.
`rateProjection` | double | The increase rate at which to project the limit.

[Back to Annual Limits](RBLe.AnnualLimits.md)