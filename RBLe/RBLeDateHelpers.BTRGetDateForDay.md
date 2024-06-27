# BTRGetDateForDay Function

Given a `startDate` date and day of week, find the next date whose day of the week equals `desiredDay` and `dateType`.

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