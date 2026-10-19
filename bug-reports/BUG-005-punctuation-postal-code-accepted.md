# BUG-005: Punctuation Accepted in Checkout Postal Code

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
3. Enter `!!!` in the Postal Code field.
4. Click Continue.

## Expected Result

The application should enforce its intended postal-code validation rules.

## Actual Result

The application accepted punctuation in the Postal Code field, according to the recorded observation.

## Impact

If punctuation-only postal codes are invalid under the application's requirements, accepting them may allow invalid checkout information.

## Evidence

- Screenshot: [Insert actual screenshot path or filename]

## Related Test Case

- [Insert the relevant checkout validation test case ID]

## Notes

Confirm the expected postal-code format before classifying this observation as a confirmed defect.
