# BTRCoveredComp Function

A replacement function for the Cfgena.xla!CoveredComp() function.  Returns a decimal value of covered compensation at Social Security Normal Retirement Age or at yearEvent parameter.

## Syntax

```excel
=BTRCoveredComp(yearBirth, rateNAW, yearEvent, lawYear, flagTransition, optRounding)
```

Parameter | Type | Default | Description
---|---|---|---
`yearBirth` | Int32 |  | The member's year of birth.
`rateNAW` | Double? | `0.045` | NAW increase rate, defaulted to 4.5%.
`yearEvent` | Int32? | `0` | Year of requested covered compensation.
`lawYear` | Int32? | `0` | SS law year, defaulted to current law year.
`flagTransition` | Int32? | `0` | Transition rule (when value is 1, else defaulted to 0), when value is 1 then the averaging of 35 years of wage base ended at the year before yearEvent else it ended at 'yearEvent'.
`optRounding` | Int32? | `0` | Rounding, defaulted to 0, means rounded down to 12, other alues are 12 (same as 0), 1, 300, 600 or 6000 means rounded to the nearest value, else unrounded.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/RBLe.md#function-documentation)