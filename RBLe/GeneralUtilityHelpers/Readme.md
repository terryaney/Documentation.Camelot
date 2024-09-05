# General Utility Functions

Click one of the links in the following list to see detailed help about the function.

Function | Description
---|---
[`BTRContains`](BTRContains.md) | Returns whether a specified substring occurs within a string (optionally case sensitive).
[`BTREbcdicText`](BTREbcdicText.md) | Returns a EBCDIC, extended binary-coded decimal interchange code, encoded string.
[`BTREvaluate`](BTREvaluate.md) | Evaluates an Excel formula passed in.  If the formula contains one or more {K.id} tokens, each is parsed and the 'id' is used in BTRLookup to find a value to substitute into the formula
[`BTRFilter`](BTRFilter.md) | Returns a filtered table given a list of filter columns and values to compare.
[`BTRJoinLookup`](BTRJoinLookup.md) | Concatenates all values (or fallback is not found) from columnToReturn column in a table range (including column headers), using the specified separator between elements.  Similar to VLOOKUP but always does exact match, uses column names instead of numbers (prevents issues when columns are inserted or removed), can search specified column instead of always the first, and provides ability to give a default.
[`BTRLookup`](BTRLookup.md) | Returns the value (or fallback is not found) from columnToReturn column in a table range (including column headers).  Similar to VLOOKUP but always finds exact match, uses column names instead of numbers (prevents issues when columns are inserted or removed), can search specified column instead of always the first, and provides ability to give a default.
[`BTRToCamelCase`](BTRToCamelCase.md) | Returns a camelCase string from a spine-case string.
[`BTRToInputName`](BTRToInputName.md) | Returns an iInputName from a spine-case string.
[`BTRToxDSName`](BTRToxDSName.md) | Returns a spine-cased xDS name from PascalCase or iInputName input string.


[Back to RBLe Framework](/RBLe/Readme.md)