# BTRSSNRD Function

A replacement function for the Cfgena.xla!SSNRD() function.  Returns a decimal value representing the Social Security normal retirement date.

## Syntax

```excel
=BTRSSNRD(dateBirth, simplifiedResultsArg)
```

Parameter | Type | Default | Description
---|---|---|---
`dateBirth` | DateTime | `` | The member's date of birth.
`simplifiedResultsArg` | Boolean? | `false` | Simplified integer values (e.g. for Covered Compensation and IRC 415 limit purposes), otherwise actual values for Social Security use.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)