# BTRWageBase Function

A replacement function for the Cfgena.xla!WageBase() function.  Returns a decimal value of Social Security Wage Base at yearEvent parameter.

## Syntax

```excel
=BTRWageBase(yearEvent, rateNAW, lawYear, unrounded)
```

Parameter | Type | Default | Description
---|---|---|---
`yearEvent` | Int32 |  | Year of requested wage base.
`rateNAW` | Double? | `0.045` | NAW increase rate, defaulted to 4.5%.
`lawYear` | Int32? | `0` | SS law year, defaulted to current law year.
`unrounded` | Boolean? | `False` | Whether or not to apply the $300 rounding.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](..\RBLe.md#function-documentation)