# BUG-004: Alphabetic Characters Accepted in Checkout Postal Code

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

1. Enter `Test` in the First Name field.
2. Enter `User` in the Last Name field.
3. Enter `ABCDEF` in the Postal Code field.
4. Click Continue.

## Expected Result

The application should enforce the postal-code format specified by its requirements.

## Actual Result

The application accepted alphabetic characters in the Postal Code field, according to the recorded observation.

## Impact

If the application requires a particular postal-code format, accepting unsupported characters may result in invalid checkout information.

## Evidence

- Screenshot: evidence/Screenshots/wrong password.png

## Notes

Postal codes can contain letters in some countries. The intended format must be established before this behavior can be classified as a defect.
