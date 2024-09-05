# BTRSplit Function

Returns an array of values by splitting the provided delimitted string.  If index is provided, returns a single value at the specified 1 based array index.

## Syntax

```excel
=BTRSplit(listValues, delimiter, index, indexOutOfRangeDefault)
```

Parameter | Type | Default | Description
---|---|---|---
`listValues` | String |  | Delimmited list of values to split into an array.
`delimiter` | String? | `","` | Optional.  Single character used to delimit the list.  Comma is the default.
`index` | Int32? |  | Optional.  If BTRSplit is not sheet array formula, but used inline in cell formula, can provide 1 based index of value to return to eliminate need of INDEX() call.
`indexOutOfRangeDefault` | String? |  | Optional.  If index is provided and is out of range of the values array, return this as the value.  Default is to return #VALUE.

[Back to Formatting](Readme.md) | [Back to All RBLe Functions](..\RBLe.md#function-documentation)