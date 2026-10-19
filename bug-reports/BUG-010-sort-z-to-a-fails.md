# BUG-010: Z–A Inventory Sorting Does Not Work Correctly

**Status:** Observed  
**Module:** Inventory / Sorting  
**Test Account:** `visual_user`  
**Severity:** Minor  
**Priority:** Low

**Related Requirement:** REQ-05

## Environment

- Application: SauceDemo — https://www.saucedemo.com/
- Browser: edge
- Operating system: Windows 11-25H2/ 26200.9711
- Test date: 18th October 2026

## Preconditions

1. Log in using `visual_user`.
2. Navigate to the inventory page.

## Steps to Reproduce

1. Open the sorting dropdown.
2. Select Name (Z to A).
3. Inspect the product order.

## Expected Result

Products should appear in reverse alphabetical order by name.

## Actual Result

The Z–A sorting option did not work correctly, according to the recorded observation.

## Impact

Users may be unable to locate products using reverse alphabetical sorting.

