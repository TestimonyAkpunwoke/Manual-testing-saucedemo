# BUG-002: Numeric Characters Accepted in Checkout First Name

**Status:** Observed — validation rule needs confirmation  
**Module:** Checkout Information  
**Test Account:** `standard_user`  
**Severity:** Undetermined  
**Priority:** Undetermined  
**Related Requirement:** REQ-08

## Environment

- Application: [SauceDemo](https://www.saucedemo.com/)
- Browser: Edge
- Operating System: Windows 11/155
- Test Date: 18th october, 2026

## Preconditions

1. Log in as `standard_user`.
2. Add a product to the cart.
3. Navigate to the checkout information page.

## Steps to Reproduce

1. Enter `12345` in the First Name field.
2. Enter `Test` in the Last Name field.
3. Enter `100001` in the Postal Code field.
4. Click Continue.

## Expected Result

The application should enforce the intended first-name validation rule.

## Actual Result

The application accepted numeric characters in the First Name field, according to the recorded observation.

## Impact

If numeric-only names are prohibited by the product requirements, accepting them may allow invalid customer information into checkout.

## Evidence

- Screenshot: [Insert actual screenshot path or filename]

## Related Test Case

- [Insert the relevant checkout validation test case ID]

## Notes

REQ-08 requires checkout-field validation but does not explicitly specify permitted first-name characters. Confirm the intended rule before classifying this observation as a confirmed defect.
