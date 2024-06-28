# BTRGetMacroVariable Function

Returns variable value set during macro processing.  If not during macro processing, this returns null.

## Syntax

```excel
=BTRGetMacroVariable(name)
```

Parameter | Type | Default | Description
---|---|---|---
`name` | String | `""` | The name of the variable stored via SetVariable action during RBLe Macro processing you wish to retrieve.  This is a placeholder function returning 'empty' when used in Excel, but during ProcessWorkbook execution it evaluates properly.

[Back to RBLe Macro](RBLeRBLeMacro.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)