# BTRAnnualReturnDebug Function

Debug version of BTRAnnualReturn that returns value or exception string (instead of #VALUE on error).  DOC: Han, Cfgena replacement?  Returns plan investment annual return based on Fund allocations and how Funds are mapped to assets classes.

## Syntax

```excel
=BTRAnnualReturnDebug(tableName, planType, year, yearCurrent, fundAllocations, inputAllocations, returnByClass, fundIndex)
```

Parameter | Type | Default | Description
---|---|---|---
`tableName` | String |  | Required.  Fund Table Name.
`planType` | Int32 |  | Required.  Plan type.
`year` | Int32 |  | Required.  Year of requested returns.
`yearCurrent` | Int32 |  | Required.  Current year.
`fundAllocations` | Double[,] |  | Required.  Current fund allocations.
`inputAllocations` | Double[,] |  | Required.  Entered fund allocations (this will override current or future allocations).
`returnByClass` | Double[,] |  | Required.  Array of investment returns by assets classes.
`fundIndex` | String |  | Optional.  If provided allocation will be changed 100% to that target fund.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)