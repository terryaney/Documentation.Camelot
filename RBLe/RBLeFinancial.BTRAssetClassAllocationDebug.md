# BTRAssetClassAllocationDebug Function

Debug version of BTRAssetClassAllocation that returns value or exception string (instead of #VALUE on error).  DOC: Han, Cfgena replacement?  Returns plan asset class allocation based on Fund allocations and how Funds are mapped to assets classes.

## Syntax

```excel
=BTRAssetClassAllocationDebug(tableName, planType, year, fundAllocations, inputAllocations, fundIndex)
```

Parameter | Type | Description
---|---|---
`tableName` | String | Required.  Fund Table Name.
`planType` | Int32 | Required.  Plan type.
`year` | Int32 | Required.  Year of requested allocation.
`fundAllocations` | Double[,] | Required.  Current fund allocations.
`inputAllocations` | Object | Optional.  Entered fund allocations (this will override current or future allocations).
`fundIndex` | Object | Optional.  If provided allocation will be changed 100% to that target fund.

[Back to Financial](RBLeFinancial.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)