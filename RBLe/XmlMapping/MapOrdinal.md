# MapOrdinal Function

Returns the current ordinal position of the current element being processed.  If 'scopeDepth' is passed, it is the current ordinal position of the ancestor mapping element determined by 'scopeDepth' levels.  Placeholder returning defaultValue in Excel.

## Syntax

```excel
=MapOrdinal(scopeDepth, defaultValue)
```

Parameter | Type | Default | Description
---|---|---|---
`scopeDepth` | Int32? | `1` | How many parent levels to walk back up to determine mapping scope.  Default value is one.
`defaultValue` | Int32? | `1` | Value to return to make coding specification formulas easier.

[Back to Xml Mapping](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)