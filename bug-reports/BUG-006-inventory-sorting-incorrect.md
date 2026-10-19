# BUG-006: Inventory Sorting Behaves Incorrectly

**Status:** Observed — specific failing options to be recorded  
**Module:** Inventory / Sorting  
**Test Account:** `problem_user`  
**Severity:** Undetermined  
**Priority:** Undetermined  
**Related Requirement:** REQ-05

## Environment

- Application: SauceDemo — https://www.saucedemo.com/
- Browser: edge
- Operating system: Windows 11-25H2/ 26200.9711
- Test date: 18th October 2026

## Preconditions

1. Log in using `problem_user`.
2. Navigate to the inventory page.

## Steps to Reproduce

1. Open the inventory sorting dropdown.
2. Select the sorting option you observed failing.
3. Inspect the order of the displayed products.
4. Compare the displayed order with the selected sorting direction.

## Expected Result

Products should be sorted according to the selected alphabetical or price-based option.

## Actual Result

Inventory sorting did not behave correctly for `problem_user`, according to the recorded observation.

## Impact

Incorrect sorting makes it harder for users to find and compare products.


## Notes

Use the existing evidence to specify exactly which sorting options failed. Avoid claiming that all four options failed unless your records support that conclusion.
