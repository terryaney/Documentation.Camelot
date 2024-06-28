# BTRDateDiff Function

Returns difference in years, months, full months (integer) or days between two dates.

## Syntax

```excel
=BTRDateDiff(start, end, interval, inclusive)
```

Parameter | Type | Default | Description
---|---|---|---
`start` | DateTime |  | The start date.
`end` | DateTime |  | The end date.
`interval` | Object? |  | Optional.  1 for Years, 2 for Months, 3 for FullMonths and 4 for Days.  Default is 1.
`inclusive` | Object? |  | Optional.  Whether or not to include the last day as part of the calculation.  Default is false.

[Back to Date Helpers](RBLeDateHelpers.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)