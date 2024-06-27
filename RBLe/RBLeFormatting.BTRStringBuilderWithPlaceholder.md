# BTRStringBuilderWithPlaceholder Function

Builds a string using the template with zero based subsitution tokens (i.e. {0}, {1}, ...) and substitutes them for the supplied parameters.

## Syntax

```excel
=BTRStringBuilderWithPlaceholder(placeHolders, template, parameters)
```

Parameter | Type | Description
---|---|---
`placeHolders` | String | A space delimitted open and closing placeholder to use for token matching (i.e. `{{ }}`, `<< >>`, or `< >`).
`template` | String | The string template to use in the builder with zero based subsitution tokens (i.e. `{0}`, `{1}`, ...).
`parameters` | Object[] | The parameters to substitute into the string template.

[Back to Formatting](RBLeFormatting.md)