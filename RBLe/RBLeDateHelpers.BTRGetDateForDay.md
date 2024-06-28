# BTRGetDateForDay Function

Given a `startDate` date and day of week, find the next date whose day of the week equals `desiredDay` and `dateType`.

## Remarks

If `startDate.DayOfWeek` equals `desiredDay` and `dateType` is `Next` or `Previous`, `startDate` is returned.  
If `dateType` is `PreviousWeek` or `NextWeek`, the `desiredDay` before the previous Sunday or after the next Sunday, respectively, will be returned.  
If `dateType` is `Previous` or `Next`, the first occurrence of the `desiredDay` in the appropriate direction will be returned.  
`desiredDay` can be abbreviated to `mon`, `tue`, `wed`, `thu`, `fri`, `sat`, and `sun`.  
`dateType` can be abbreviated to `pw`, `prevweek`, `nw`, `pd`, `prevday`, `previous`, `prev`, `nd`, and `next`.
## Syntax

```excel
=BTRGetDateForDay(startDate, desiredDay, dateType)
```

Parameter | Type | Description
---|---|---
`startDate` | DateTime | The target date.
`desiredDay` | String | Monday, Tuesday, ..., Friday representing which day you want.
`dateType` | String | Date increment type.  `PreviousWeek`, `NextWeek`, `PreviousDay`, `NextDay`.

[Back to Date Helpers](RBLeDateHelpers.md)