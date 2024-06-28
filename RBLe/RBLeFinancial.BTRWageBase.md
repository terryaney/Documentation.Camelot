# BTRWageBase Function

A replacement function for the Cfgena.xla!WageBase() function.  Returns a decimal value of Social Security Wage Base at yearEvent parameter.

## Syntax

```excel
=BTRWageBase(yearEvent, rateNAW, lawYear, unrounded)
```

Parameter | Type | Description
---|---|---
`yearEvent` | Int32 | Year of requested wage base.
`rateNAW` | Object | NAW increase rate, defaulted to 4.5%.
`lawYear` | Int32 | SS law year, defaulted to current law year.
`unrounded` | Boolean | Whether or not to apply the $300 rounding.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)