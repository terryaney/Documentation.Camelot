# BTRAssetClassAllocation Function

DOC: Han, Cfgena replacement?  Returns plan asset class allocation based on Fund allocations and how Funds are mapped to assets classes.

## Syntax

```excel
=BTRAssetClassAllocation(tableName, planType, year, fundAllocations, inputAllocations, fundIndex)
```

Parameter | Type | Default | Description
---|---|---|---
`tableName` | String |  | Required.  Fund Table Name.
`planType` | Int32 |  | Required.  Plan type.
`year` | Int32 |  | Required.  Year of requested allocation.
`fundAllocations` | Double[,] |  | Required.  Current fund allocations.
`inputAllocations` | Double[]? |  | Optional.  Entered fund allocations (this will override current or future allocations).
`fundIndex` | String? |  | Optional.  If provided allocation will be changed 100% to that target fund.

[Back to Financial](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)