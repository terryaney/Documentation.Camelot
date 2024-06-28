# BTRSSPIASalHist Function

A replacement function for the Cfgena.xla!SSTableProj() function using a pay array.  Returns a decimal value representing the age 65 Social Security monthly benefit using exact pays.

## Syntax

```excel
=BTRSSPIASalHist(dateBirth, dateEvent, ageRetire, actualPay, rateNAW, rateFuturePay, rateBackPay, addNAWToBackPay, rateCOLA, lastPayYear, lawYear, futurePayType, firstPayAge, stopNAWGrowth, postNRDIncrease, yearCOLAStops)
```

Parameter | Type | Description
---|---|---
`dateBirth` | DateTime | The member's date of birth.
`dateEvent` | DateTime | The member's date of event (i.e. Date Term).
`ageRetire` | Double | The member's age at retirement.
`actualPay` | Double[] | The member's annual compensations ending at current Social Security year.  Annual compensation will be projected for any missing years from age 18 through the year before payment start.
`rateNAW` | Double | NAW increase rate.
`rateFuturePay` | Double | Future pay increase rate.
`rateBackPay` | Double | Backward pay increase rate.
`addNAWToBackPay` | Boolean | Add NAW to backward pay increase rate (TRUE or FALSE).
`rateCOLA` | Double | CPI increase rate.
`lastPayYear` | Int32 | Ending year of compensation in the compensation array.
`lawYear` | Int32 | Social Security law year.
`futurePayType` | String | Type of pay after the year before termination year: C=project one more year at rateFuturePay then stay constant till the year before commencement year, L= stay constant till the year before commencement year., Z=zero pay starting termination year.
`firstPayAge` | Int32 | The first age when emeber started receiving compensation.
`stopNAWGrowth` | Boolean | Stop NAW growth after termination?
`postNRDIncrease` | Boolean | Include post NRD increase?
`yearCOLAStops` | Int32 | Year COLA Stops

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)