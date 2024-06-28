# BTRPV Function

Calculates the present value of a loan or an investment, based on a variable, multiple interest rates.

## Syntax

```excel
=BTRPV(period, interestRates, paymentAmounts, paymentTiming)
```

Parameter | Type | Description
---|---|---
`period` | Int32 | Required. The total number of periods to calculate.  For both interestRates and paymentAmounts, if the period is greater than number of elements present in each array, the array is padded to the end using the last element provided.
`interestRates` | Double[] | Required. The interest rates per period. For example, if you obtain an automobile loan at a 10 percent annual interest rate and make monthly payments, your interest rate per month is 10%/12, or 0.83%. You would enter 10%/12, or 0.83%, or 0.0083, into the formula as the rate.
`paymentAmounts` | Double[] | Required. The payment amounts made each period. Typically, each amount includes principal and interest but no other fees or taxes. For example, a monthly payment on a $10,000, four-year car loan at 12 percent is $263.33. You would enter -263.33 into the formula as one of the amounts.
`paymentTiming` | Int32 | Optional. The number 0 (at the end of the period) or 1 (at the beginning of the period) and indicates when payments are due.  The default is 0.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)