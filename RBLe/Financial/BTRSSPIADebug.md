# BTRSSPIADebug Function

Debug version of BTRSSPIA that returns value or exception string (instead of #VALUE on error).  A replacement function for the Cfgena.xla!SSExactPays() function using a single current pay value.  Returns a decimal value representing the age 65 Social Security monthly benefit using exact pays.

## Syntax

```excel
=BTRSSPIADebug(dateBirth, dateEvent, ageRetire, payCurrent, rateNAW, rateFuturePay, rateBackPay, addNAWToBackPay, rateCOLA, lawYear, futurePayType, firstPayAge, stopNAWGrowth, lastPayYear, postNRDIncrease, yearCOLAStops)
```

Parameter | Type | Default | Description
---|---|---|---
`dateBirth` | DateTime |  | The member's date of birth.
`dateEvent` | DateTime |  | The member's date of event (i.e. Date Term).
`ageRetire` | Double |  | The member's age at retirement.
`payCurrent` | Double |  | The member's annual compensation for current Social Security year.  Annual compensation will be projected for any missing years from age 18 through the year before payment start.
`rateNAW` | Double? | `0.045` | NAW increase rate.
`rateFuturePay` | Double? | `0.05` | Future pay increase rate.
`rateBackPay` | Double? | `0` | Backward pay increase rate.
`addNAWToBackPay` | Boolean? | `true` | Add NAW to backward pay increase rate (TRUE or FALSE).
`rateCOLA` | Double? | `0.04` | CPI increase rate.
`lawYear` | Int32? | `0` | Social Security law year.
`futurePayType` | String? | `"C"` | Type of pay after the year before termination year: C=project one more year at rateFuturePay then stay constant till the year before commencement year, L= stay constant till the year before commencement year., Z=zero pay starting termination year.
`firstPayAge` | Int32? | `18` | The first age when emeber started receiving compensation.
`stopNAWGrowth` | Boolean? | `true` | Stop NAW growth after termination?
`lastPayYear` | Int32? | `0` | Last pay year
`postNRDIncrease` | Boolean? | `true` | Include post NRD Increase?
`yearCOLAStops` | Int32? | `0` | Year COLA Stops

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)