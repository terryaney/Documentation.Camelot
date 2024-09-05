# Formatting Functions

BTR has introduced some helper functions that can be used to format values in desired formats supporting culture localization. For number formatting, see Standard Numeric Format Strings and Custom Numeric Format Strings. For date formatting, see Standard Date and Time Format Strings and Custom Date and Time Format Strings.

Click one of the links in the following list to see detailed help about the function.

Function | Description
---|---
[`BTRDateFormat`](BTRDateFormat.md) | Formats a Date value to a string representation using the specified format and culture-specific format information.
[`BTRJoin`](BTRJoin.md) | Joins a range of text strings into one string using seperator.
[`BTRNumberFormat`](BTRNumberFormat.md) | Formats a numeric value to a string representation using the specified format and culture-specific format information.
[`BTRResourceString`](BTRResourceString.md) | Returns localized resource string.
[`BTRSplit`](BTRSplit.md) | Returns an array of values by splitting the provided delimitted string.  If index is provided, returns a single value at the specified 1 based array index.
[`BTRStringBuilder`](BTRStringBuilder.md) | Builds a string using the template with zero based subsitution tokens (i.e. `{0}`, `{1}`, ...) and substitutes them for the supplied parameters.
[`BTRStringBuilderWithPlaceholder`](BTRStringBuilderWithPlaceholder.md) | Builds a string using the template with zero based subsitution tokens (i.e. {0}, {1}, ...) and substitutes them for the supplied parameters.
[`BTRTextJoin`](BTRTextJoin.md) | Concatenates a list or range of text strings using a delimiter. Polyfill for non-supported Excel TEXTJOIN function.
[`BTRUnique`](BTRUnique.md) | Returns a list of unique values from a given input range.


[Back to RBLe Framework](/RBLe/Readme.md)