# BTRNAW Function

A replacement function for the Cfgena.xla!SSNAW() function.  Returns a decimal value of Social Security National Average Wage Base at yearEvent parameter.

## Syntax

```excel
=BTRNAW(yearEvent, rateNAW, lawYear)
```

Parameter | Type | Default | Description
---|---|---|---
`yearEvent` | Int32 |  | Year of requested wage base.
`rateNAW` | Double? | `0.045` | NAW increase rate, defaulted to 4.5%.
`lawYear` | Int32? | `0` | SS law year, defaulted to current law year.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)