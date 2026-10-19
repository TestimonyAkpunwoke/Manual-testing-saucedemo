# BUG-011: Price Low-to-High Sorting Does Not Work Correctly

**Status:** Observed  
**Module:** Inventory / Sorting  
**Test Account:** `visual_user`  
**Severity:** Undetermined  
**Priority:** Undetermined  
**Related Requirement:** REQ-05

## Environment

- Application: [SauceDemo](https://www.saucedemo.com/)
- Browser: [Enter browser and version]
- Operating System: [Enter OS]
- Test Date: [Enter date]

## Preconditions

1. Log in using `visual_user`.
2. Navigate to the inventory page.

## Steps to Reproduce

1. Open the sorting dropdown.
2. Select Price (low to high).
3. Inspect the displayed product prices and their order.

## Expected Result

Products should appear in ascending price order, from lowest to highest.

## Actual Result

The price low-to-high sorting option did not work correctly, according to the recorded observation.

## Impact

Users may be unable to compare products in ascending price order.

## Evidence

- Screenshot: [Insert actual screenshot path or filename]

## Related Test Case

- [Insert the price low-to-high sorting test case ID]
