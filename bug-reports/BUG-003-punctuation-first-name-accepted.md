# BUG-003: Punctuation Accepted in Checkout First Name

**Status:** Observed — validation rule needs confirmation  
**Module:** Checkout Information  
**Test Account:** `standard_user`  
**Severity:** Undetermined  
**Priority:** Undetermined  
**Related Requirement:** REQ-08

## Environment

- Application: SauceDemo — https://www.saucedemo.com/
- Browser: edge
- Operating system: Windows 11-25H2/ 26200.9711
- Test date: 18th October 2026

## Preconditions

1. Log in as `standard_user`.
2. Add a product to the cart.
3. Navigate to the checkout information page.

## Steps to Reproduce

1. Enter `!!!` in the First Name field.
2. Enter `Test` in the Last Name field.
3. Enter `100001` in the Postal Code field.
4. Click Continue.

## Expected Result

The application should enforce its intended first-name validation rules.

## Actual Result

The application accepted punctuation in the First Name field, according to the recorded observation.

## Impact

If punctuation-only names are prohibited, this behavior may allow invalid customer information into checkout.

## Notes

The current requirement does not explicitly define allowed characters. Confirm the intended rule before classifying this observation as a confirmed defect.
