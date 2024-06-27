# Validation Functions

KAT has introduced some helper functions that can be used to validate calculation inputs and report errors via the `error` table if necessary.

Click one of the links in the following list to see detailed help about the function.

Function | Description
---|---
[`BTRLogicAll`](RBLeValidation.BTRLogicAll.md) | Returns 1 if all keys provided evaluate to not 'false' (#error, 0, FALSE) or 0 if any key provided is 'false'.  Each 'key' is a lookup into provided table, and the 'value' column is evalated for 'false'.
[`BTRLogicAny`](RBLeValidation.BTRLogicAny.md) | Returns 1 if any key provided evaluates to not 'false' (#error, 0, FALSE) or 0 if all keys provided are 'false'.  Each 'key' is a lookup into provided table, and the 'value' column is evalated for 'false'.
[`BTRLogicIfElse`](RBLeValidation.BTRLogicIfElse.md) | Given param array of {condition1}, {expression1}, {condition2}, {expression2}, .., {conditionN, {expressionN}, returns expression value for the first condition that evalates to true.  If all conditions are false, returns #NA.
[`BTRLogicIn`](RBLeValidation.BTRLogicIn.md) | Returns 1 if 'value' is present anywhere in the 'table' parameter.
[`BTROnAll`](RBLeValidation.BTROnAll.md) | Returns 1 if all parameters provided evaluate to not 'false' (#error, 0, FALSE, '') or 0 if any parameter provided is 'false'.
[`BTROnAny`](RBLeValidation.BTROnAny.md) | Returns 1 if any parameters provided evaluate to not 'false' (#error, 0, FALSE, '') or 0 if all parameters provided are 'false'.
[`BTRParseAgeDate`](RBLeValidation.BTRParseAgeDate.md) | Validates and converts the input string representation of an age/date, supporting culture specific formats, to its Date equivalent.  Throws an exception if not a valid age/date.
[`BTRParseDate`](RBLeValidation.BTRParseDate.md) | Validates and converts the input string representation of a date and time, supporting culture specific formats, to its Date equivalent.  Throws an exception if not a valid date.
[`BTRParseDecimal`](RBLeValidation.BTRParseDecimal.md) | Validates and converts the input string representation of a number to its decimal equivalent.
[`BTRParseInteger`](RBLeValidation.BTRParseInteger.md) | Validates and converts the input string representation of a number to its integer (no decimals) equivalent.
[`BTRValidateAgeDate`](RBLeValidation.BTRValidateAgeDate.md) | Returns an integer indicating whether an input string is a valid age/date and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateDate`](RBLeValidation.BTRValidateDate.md) | Returns an integer indicating whether an input string is a valid date and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateDecimal`](RBLeValidation.BTRValidateDecimal.md) | Returns an integer indicating whether an input string is a valid decimal value and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateInteger`](RBLeValidation.BTRValidateInteger.md) | Returns an integer indicating whether an input string is a valid integer and within specified range. -1 if invalid, 0 if valid and in range, and 1 if outside of range.
[`BTRValidateRegEx`](RBLeValidation.BTRValidateRegEx.md) | Returns whether the regular expression finds a match in the input string.
[`BTRValidateRoutingNumber`](RBLeValidation.BTRValidateRoutingNumber.md) | Returns whether the provided input is a valid US banking routing number.


[Back to RBLe Framework](RBLe.md)