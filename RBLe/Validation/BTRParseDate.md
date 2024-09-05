# BTRParseDate Function

Validates and converts the input string representation of a date and time, supporting culture specific formats, to its Date equivalent.  Throws an exception if not a valid date.

## Syntax

```excel
=BTRParseDate(value, culture, allowedFormats, validDates)
```

Parameter | Type | Default | Description
---|---|---|---
`value` | String |  | A string that contains a date and time to convert.
`culture` | String? | `"en-US"` | A string that supplies culture-specific format information about `value`.
`allowedFormats` | String? |  | A `\|` delimitted string that supplies a list of allowable formats to attempt to parse `value`.
`validDates` | String? |  | A `,` delimitted string of allowable dates to validate in the format of 1..N, Last, Mon-Sun, Mon-Sun.[N\|Last] (Nth occurence of or last day in month), or W1-W5 (first through the fifth week of month).  If pattern starts with `!`, it is a 'not' check.

[Back to Validation](Readme.md) | [Back to All RBLe Functions](/RBLe/Readme.md#function-documentation)