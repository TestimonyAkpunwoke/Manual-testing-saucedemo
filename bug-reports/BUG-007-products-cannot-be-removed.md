# BUG-007: Some Products Cannot Be Removed from Inventory

**Status:** Observed  
**Module:** Inventory / Cart  
**Test Account:** `problem_user`  
**Severity:** Undetermined  
**Priority:** Undetermined  
**Related Requirement:** REQ-06

## Environment

- Application: SauceDemo — https://www.saucedemo.com/
- Browser: edge
- Operating system: Windows 11-25H2/ 26200.9711
- Test date: 18th October 2026

## Preconditions

1. Log in using `problem_user`.
2. Navigate to the inventory page.
3. Add the relevant product or products to the cart.

## Steps to Reproduce

1. Locate a product that you previously added to the cart.
2. Attempt to remove it using the inventory-page control.
3. Observe the button behavior and cart badge.

## Expected Result

The selected product should be removed from the cart, and the cart badge should update accordingly.

## Actual Result

Some products could not be removed from the inventory page, according to the recorded observation.

## Impact

Users may be unable to correct their cart selections from the inventory page.

## Evidence

- Screenshot: [Insert actual screenshot path or filename]

## Related Test Case

- [Insert the relevant cart removal test case ID]

## Notes

Identify the affected product or products using your existing evidence if available.
