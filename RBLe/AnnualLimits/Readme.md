# Annual Limits Functions

This module contains procedures used to return various contribution and salary limits.

*CFGENA has following remarks. Not sure if we are implementing them or if we need them?*

Results: This function returns 9.999999e19 (a very large value) as the value of the limit if no limit was in effect for that year. For example, this would be the result for Medicare Wage Base for years after 1993.

The function returns an error when the limit is not available. This could mean that: (a) the law implementing the limit occurred after the year you specified; (b) the function does not contain limits as far back as the year you specified; or (c) the law was revised to the extent that the limit no longer applies (as in the case of HCE upper and lower limits).

You can make the function return n/a (as a string, not the N/A Excel error), when a limit is not available by placing an exclamation point in front of Name. With an exclamation point, the result does not produce a CFGENA error when the limit is not available.

Note that rounding also enables a according to the law mode. That is, according to the law, many of the rounded values are not allowed to be less than the value for some limit-specific year. This becomes an issue when, like in 2010, the actual COLA was less than zero and produced unrounded limits that were less than those for 2009. This means, that the function will return the same values (for many limits) for 2010 as it does for 2009. If you ask the function to produce unrounded numbers, this extra test is not done.

Projecting limits: projection is done from the unrounded limit then the appropriate rounding is applied.

By placing an asterisk in front of Name (within the quotes), the unrounded limit is returned (if applicable). For example, AnnualLimit (*415DBLimit, 2001,0.0,2001) would yield $141,075 rather than $140,000.

Click one of the links in the following list to see detailed help about the function.

Function | Description
---|---
[`BTR401A17Max`](BTR401A17Max.md) | A replacement function for the Cfgena.xla!AnnualLimits() function call with '401(a)(17)PayLimit' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum compensation recognized under qualified pension or profit sharing plans (ignores EGTRRA limit changes). Post-2001 limits are updated each year with the annual CPI/W rate.
[`BTR401kMax`](BTR401kMax.md) | A replacement function for the Cfgena.xla!AnnualLimits() function call with 'Max401(k)Contribution' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum permitted salary deferral under §401(k).
[`BTR403bMax`](BTR403bMax.md) | DOC: Han, Cfgena replacement?  Returns an integer value representing maximum permitted salary deferral under §403(b).
[`BTR415DBMax`](BTR415DBMax.md) | A replacement function for the Cfgena.xla!AnnualLimits() function call with '415DBLimit' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum annual defined benefit payable at Social Security normal retirement age under §415(b).
[`BTR415DCMax`](BTR415DCMax.md) | A replacement function for the Cfgena.xla!AnnualLimits() function call with '415DCLimit' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum Annual Addition under §415(c). Applies to total (including company) contributions.
[`BTR457bMax`](BTR457bMax.md) | DOC: Han, Cfgena replacement?  Returns an integer value representing maximum permitted salary deferral under §457(b).
[`BTRCatchupMax`](BTRCatchupMax.md) | A replacement function for the Cfgena.xla!AnnualLimits() function call with 'Max401(k)Make-up' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing maximum make-up contribution permitted for 50+ year-olds under §401(k).
[`BTRHCELimit`](BTRHCELimit.md) | A replacement function for the Cfgena.xla!AnnualLimits() function call with 'HCECompLimit' name parameter in favor of explicit function name (reduces parameter typo errors).  Returns an integer value representing annual compensation used to define highly compensated employee after 1996.


[Back to RBLe Framework](/RBLe/RBLe.md)