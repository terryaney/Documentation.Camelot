# BTRGetDateForDay Function

Given a `startDate` date and day of week, find the next date whose day of the week equals `desiredDay` and `dateType`.

**Returns:** `startDate` converted to the first day of the month coincident or following.
## Remarks

1. If `startDate.DayOfWeek` equals `desiredDay` and `dateType` is `Next` or `Previous`, `startDate` is returned.  
1. If `dateType` is `PreviousWeek` or `NextWeek`, the `desiredDay` before the previous Sunday or after the next Sunday, respectively, will be returned.  
1. If `dateType` is `Previous` or `Next`, the first occurrence of the `desiredDay` in the appropriate direction will be returned.  
1. `desiredDay` can be abbreviated to `mon`, `tue`, `wed`, `thu`, `fri`, `sat`, and `sun`.  
1. `dateType` can be abbreviated to `pw`, `prevweek`, `nw`, `pd`, `prevday`, `previous`, `prev`, `nd`, and `next`.
## Syntax

```excel
=BTRGetDateForDay(startDate, desiredDay, dateType)
```

Parameter | Type | Default | Description
---|---|---|---
`startDate` | DateTime |  | The target date.
`desiredDay` | String |  | Monday, Tuesday, ..., Friday representing which day you want.
`dateType` | String |  | Date increment type.  `PreviousWeek`, `NextWeek`, `PreviousDay`, `NextDay`.

[Back to Date Helpers](RBLeDateHelpers.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)