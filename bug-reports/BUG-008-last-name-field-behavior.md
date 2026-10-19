# BUG-008: Checkout Last-Name Field Does Not Accept Entered Value

**Status:** Observed — exact behavior to be described from evidence  
**Module:** Checkout Information  
**Test Account:** `problem_user`  
**Severity:** Undetermined  
**Priority:** Undetermined  
**Related Requirement:** REQ-08

## Environment

- Application: [SauceDemo](https://www.saucedemo.com/)
- Browser: [Enter browser and version]
- Operating System: [Enter OS]
- Test Date: [Enter date]

## Preconditions

1. Log in using `problem_user`.
2. Add a product to the cart.
3. Navigate to the checkout information page.

## Steps to Reproduce

1. Enter the first name.
2. Enter the last name that produced the observed behavior.
3. Complete the remaining required field.
4. Observe the last-name field and attempt to continue checkout as performed during the original test.

## Expected Result

The checkout form should accept a valid last name and allow the user to continue when all required fields are valid.

## Actual Result

The last-name field did not accept the entered last name, according to the recorded observation.

## Impact

The behavior may prevent users from completing checkout if valid last-name input is rejected.

## Evidence

- Screenshot: [Insert actual screenshot path or filename]

## Related Test Case

- [Insert the relevant checkout validation test case ID]

## Notes

Use your original evidence to describe precisely what happened. Do not assume the field was read-only, cleared the input, or blocked submission unless that was what you observed.
