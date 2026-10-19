# BUG-001: Product image does not match the product

**Status:** Observed — documented  
**Module:** Inventory / Product Display  
**Test account:** `problem_user`  
**Severity:** Minor 
**Priority:** Medium  
**Related requirement:** REQ-04 — The inventory page lists all products with name, description, price and image.

## Environment

- Application: SauceDemo — https://www.saucedemo.com/
- Browser: edge
- Operating system: Windows 11-25H2/ 26200.9711
- Test date: 18th October 2026

## Preconditions

1. The SauceDemo application is accessible.
2. The `problem_user` account is available.

## Steps to reproduce

1. Open the SauceDemo login page.
2. Log in using `problem_user` and the shared test password.
3. Navigate to the inventory page.
4. Locate the Sauce Labs Backpack product.
5. Inspect the product image displayed beside the product information.

## Expected result

The backpack product should display an image representing the backpack.

## Actual result

The backpack product displays a dog image instead of the expected backpack image.

## Evidence

Attach or reference the screenshot captured during testing:

`evidence/Screenshots/text and image misalignment.png`

## Impact

The incorrect image can confuse users about the product being displayed and reduces the accuracy and consistency of the product catalogue.


## Notes

This report documents the observed behavior for `problem_user`. The severity and priority are provisional and may be adjusted based on the project's defect classification criteria.
