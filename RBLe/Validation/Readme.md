# Validation Functions

KAT has introduced some helper functions that can be used to validate calculation inputs and report errors via the `error` table if necessary.

Click one of the links in the following list to see detailed help about the function.

Function | Description
---|---
[`BTRLogicAll`](Validation\BTRLogicAll.md) | Returns 1 if all keys provided evaluate to not 'false' (#error, 0, FALSE) or 0 if any key provided is 'false'.  Each 'key' is a lookup into provided table, and the 'value' column is evalated for 'false'.
[`BTRLogicAny`](Validation\BTRLogicAny.md) | Returns 1 if any key provided evaluates to not 'false' (#error, 0, FALSE) or 0 if all keys provided are 'false'.  Each 'key' is a lookup into provided table, and the 'value' column is evalated for 'false'.
[`BTRLogicIfElse`](Validation\BTRLogicIfElse.md) | Given param array of {condition1}, {expression1}, {condition2}, {expression2}, .., {conditionN, {expressionN}, returns expression value for the first condition that evalates to true.  If all conditions are false, returns #NA.
[`BTRLogicIn`](Validation\BTRLogicIn.md) | Returns 1 if 'value' is present anywhere in the 'table' parameter.
[`BTROnAll`](Validation\BTROnAll.md) | Returns 1 if all parameters provided evaluate to not 'false' (#error, 0, FALSE, '') or 0 if any parameter provided is 'false'.
[`BTROnAny`](Validation\BTROnAny.md) | Returns 1 if any parameters provided evaluate to not 'false' (#error, 0, FALSE, '') or 0 if all parameters provided are 'false'.
[`BTRParseAgeDate`](Validation\BTRParseAgeDate.md) | Validates and converts the input string representation of an age/date, supporting culture specific formats, to its Date equivalent.  Throws an exception if not a valid age/date.
[`BTRParseDate`](Validation\BTRParseDate.md) | Validates and converts the input string representation of a date and time, supporting culture specific formats, to its Date equivalent.  Throws an exception if not a valid date.
[`BTRParseDecimal`](Validation\BTRParseDecimal.md) | Validates and converts the input string representation of a number to its decimal equivalent.
[`BTRParseInteger`](Validation\BTRParseInteger.md) | Validates and converts the input string representation of a number to its integer (no decimals) equivalent.
[`BTRValidateAgeDate`](Validation\BTRValidateAgeDate.md) | Returns an integer indicating whether an input string is a valid age/date and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateDate`](Validation\BTRValidateDate.md) | Returns an integer indicating whether an input string is a valid date and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateDecimal`](Validation\BTRValidateDecimal.md) | Returns an integer indicating whether an input string is a valid decimal value and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateInteger`](Validation\BTRValidateInteger.md) | Returns an integer indicating whether an input string is a valid integer and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateRegEx`](Validation\BTRValidateRegEx.md) | Returns whether the regular expression finds a match in the input string.
[`BTRValidateRoutingNumber`](Validation\BTRValidateRoutingNumber.md) | Returns whether the provided input is a valid US banking routing number.


[Back to RBLe Framework](RBLe.md)