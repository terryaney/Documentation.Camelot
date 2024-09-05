# BTRLogicIfElse Function

Given param array of {condition1}, {expression1}, {condition2}, {expression2}, .., {conditionN, {expressionN}, returns expression value for the first condition that evalates to true.  If all conditions are false, returns #NA.

## Syntax

```excel
=BTRLogicIfElse(expressions)
```

Parameter | Type | Default | Description
---|---|---|---
`expressions` | Object[] |  | List of 'paired' parameters.  Each pair is condition, expression.  If condition is true, return expression.

[Back to Validation](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)