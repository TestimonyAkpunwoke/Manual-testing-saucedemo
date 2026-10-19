# BUG-009: Inventory Product Names Are Inconsistently Aligned

**Status:** Observed  
**Module:** Inventory UI  
**Test Account:** `visual_user`  
**Severity:** Major 
**Priority:** High  
**Related Requirement:** REQ-04

## Environment

- Application: SauceDemo — https://www.saucedemo.com/
- Browser: edge
- Operating system: Windows 11-25H2/ 26200.9711
- Test date: 18th October 2026

## Preconditions

1. Log in using `visual_user`.
2. Navigate to the inventory page.

## Steps to Reproduce

1. Inspect the product names across the inventory list.
2. Compare the alignment of names between product cards.

## Expected Result

Product names should follow a consistent layout and alignment.

## Actual Result

Some product names appeared left-aligned while others appeared right-aligned, according to the recorded observation.

## Impact

Inconsistent alignment reduces visual consistency and can make the inventory page harder to scan.

## Evidence

- Screenshot: evidence/Screenshots/text and image misalignment.png


## Notes

Severity and priority should reflect the impact of the visual inconsistency and your project's classification criteria.
