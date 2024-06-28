# BTRStringBuilder Function

Builds a string using the template with zero based subsitution tokens (i.e. `{0}`, `{1}`, ...) and substitutes them for the supplied parameters.

**Returns:** The string after substituting all `parameters` into the `template`.
## Remarks

The `BTRStringBuilder` method is similar to C#'s `string.Format()` function.  
  
*See Also*  
[Standard Numeric Format Strings](http://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx)  
[Custom Numeric Format Strings](http://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx)  
[Standard Date and Time Format Strings](http://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)  
[Custom Date and Time Format Strings](http://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)
## Syntax

```excel
=BTRStringBuilder(template, parameters)
```

Parameter | Type | Description
---|---|---
`template` | String | The string template to use in the builder with zero based subsitution tokens (i.e. `{0}`, `{1}`, ...).
`parameters` | Object[] | The parameters to substitute into the string template.

[Back to Formatting](RBLeFormatting.md) | [Back to All RBLe Functions](RBLe.md#function-documentation)