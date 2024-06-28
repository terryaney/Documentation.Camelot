# BTRNAW Function

A replacement function for the Cfgena.xla!SSNAW() function.  Returns a decimal value of Social Security National Average Wage Base at yearEvent parameter.

## Syntax

```excel
=BTRNAW(yearEvent, rateNAW, lawYear)
```

Parameter | Type | Description
---|---|---
`yearEvent` | Int32 | Year of requested wage base.
`rateNAW` | Double | NAW increase rate, defaulted to 4.5%.
`lawYear` | Int32 | SS law year, defaulted to current law year.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)