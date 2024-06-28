# BTRXIRR Function

Returns the internal rate of return for a schedule of cash flows that is not necessarily periodic.

## Syntax

```excel
=BTRXIRR(values, dates, iterations, maxRate, truncateTime)
```

Parameter | Type | Default | Description
---|---|---|---
`values` | Double[] | `` | Required. A series of cash flows that corresponds to a schedule of payments in dates. The first payment is optional and corresponds to a cost or payment that occurs at the beginning of the investment. If the first value is a cost or payment, it must be a negative value. All succeeding payments are discounted based on a 365-day year. The series of values must contain at least one positive and one negative value.
`dates` | Double[] | `` | Required. A schedule of payment dates that corresponds to the cash flow payments. Dates may occur in any order. Dates should be entered by using the DATE function, or as results of other formulas or functions. For example, use DATE(2008,5,23) for the 23rd day of May, 2008. Problems can occur if dates are entered as text.
`iterations` | Int32? | `25` | Optional. The default is 25.
`maxRate` | Double? | `5.0` | Optional. The default is 5.0.
`truncateTime` | Boolean? | `true` | Optional. The default is true.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)