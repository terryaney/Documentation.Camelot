# BTRCalculateLoanDebug Function

Debug version of BTRCalculateLoan that returns value or exception string (instead of #VALUE on error).  DOC: Han, Cfgena replacement?  Returns an array with 3 values: balance at EOY, principle payments with investment return at EOY and principle payments with investment return at EOB.

## Syntax

```excel
=BTRCalculateLoanDebug(balance, payPeriod, paymentPerPayPeriod, interestRate, monthEnd, returnRate, startPayPeriod, midPointCont, rounding)
```

Parameter | Type | Default | Description
---|---|---|---
`balance` | Double |  | Required. Loan balance.
`payPeriod` | Int32 |  | Required. Number of Pay period in a year.
`paymentPerPayPeriod` | Double |  | Required. Payment per pay period.
`interestRate` | Double |  | Required. Loan interest rate.
`monthEnd` | Int32 |  | Required. Calculate contributions as of the end of this month.
`returnRate` | Double |  | Required. Investment rate of return.
`startPayPeriod` | Int32? | `1` | Optional. Starting pay period. Default to 1.
`midPointCont` | Boolean? | `false` | Optional. Use mid point contributions timing calculation method.
`rounding` | Int32? | `0` | Optional. Rounding, Defaulted to 0 decimals

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)