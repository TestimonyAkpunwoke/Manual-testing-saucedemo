# Exploratory Testing Sessions — SauceDemo

## 1. Document Information

| Field | Details |
|---|---|
| Project | SauceDemo Manual QA Portfolio |
| Application | https://www.saucedemo.com/ |
| Tester | Testimony Akpunwoke |
| Test date(s) | 18th October, 2026 |
| Browser and version | Edge-25H2 |
| Operating system | 26200.9711 |
| Document status | Complete missing details from test records |

## 2. Objective

The objective of exploratory testing was to investigate application behavior beyond the predefined test cases, identify unexpected behavior, examine usability and functional issues, and record evidence for further investigation.

Testing focused on checkout information validation, inventory sorting, cart operations, product images, and interface consistency.

## 3. Scope

The following areas were explored:

- Checkout information fields
- Inventory sorting
- Adding and removing products
- Product image accuracy
- Product-name alignment
- Checkout button placement

The following test accounts were used:

- `standard_user`
- `problem_user`
- `visual_user`

## 4. Exploratory Session 1 — Checkout Input Validation

### Charter

Explore the checkout information form to understand how it handles different input types in the first-name, last-name, and postal-code fields.

### Account

`standard_user`

### Areas explored

- Numeric input in the first-name field
- Punctuation in the first-name field
- Alphabetic input in the postal-code field
- Punctuation in the postal-code field

### Observations

| ID | Observation | Result |
|---|---|---|
| EXP-01 | Numeric characters entered in the first-name field | Accepted |
| EXP-02 | Punctuation entered in the first-name field | Accepted |
| EXP-03 | Alphabetic characters entered in the postal-code field | Accepted |
| EXP-04 | Punctuation entered in the postal-code field | Accepted |

### Notes

These observations describe the behavior encountered during testing. Whether each behavior constitutes a defect depends on the intended validation requirements, which do not explicitly define permitted characters for these fields.

### Evidence

[Link or reference the screenshots captured during this session.]

### Follow-up

- Document the observations in the relevant bug reports or test notes.
- Avoid classifying input acceptance as a confirmed defect without an applicable validation rule.

## 5. Exploratory Session 2 — Inventory and Cart Behavior

### Charter

Explore inventory sorting and cart operations to identify unexpected behavior when using the `problem_user` account.

### Account

`problem_user`

### Areas explored

- Alphabetical and price-based sorting
- Removing products from the inventory page
- Product images
- Checkout last-name field behavior

### Observations

| ID | Observation | Result |
|---|---|---|
| EXP-05 | Inventory sorting by alphabet and price ranges | Did not work correctly |
| EXP-06 | Removing some products from the inventory page | Some products could not be removed |
| EXP-07 | Entering a last name during checkout | Field behaved unexpectedly |
| EXP-08 | Backpack product image | A dog image appeared instead of the backpack image |

### Notes

The exact sorting options that failed and the precise behavior of the last-name field should be described using the available screenshots or original test records. Do not infer details that were not recorded.

### Evidence

[Link or reference the screenshots captured during this session.]

### Follow-up

- Link each observation to its corresponding bug report.
- Reference relevant test cases and requirements.
- Record any uncertainty in the report rather than assuming a root cause.

## 6. Exploratory Session 3 — Visual Consistency and Sorting

### Charter

Explore the inventory interface and checkout navigation to identify presentation inconsistencies and unexpected sorting behavior.

### Account

`visual_user`

### Areas explored

- Product-name alignment
- Name sorting in both directions
- Price sorting in both directions
- Checkout button placement

### Observations

| ID | Observation | Result |
|---|---|---|
| EXP-09 | Product-name alignment | Some names appeared left-aligned and others right-aligned |
| EXP-10 | Name A–Z sorting | Worked correctly |
| EXP-11 | Name Z–A sorting | Did not work correctly |
| EXP-12 | Price high-to-low sorting | Worked correctly |
| EXP-13 | Price low-to-high sorting | Did not work correctly |
| EXP-14 | Checkout button placement | Appeared near the upper-right area and was difficult to find |

### Notes

The sorting observations are specific to the `visual_user` account. The checkout button placement is recorded as a usability concern; its classification as a defect depends on the expected layout and usability criteria.

### Evidence

[Link or reference the screenshots captured during this session.]

### Follow-up

- Link observations to the corresponding bug reports.
- Preserve the successful sorting results as well as the unsuccessful ones.
- Record the visual findings without assuming their technical cause.

## 7. Overall Findings

The exploratory sessions produced observations across checkout validation, inventory behavior, cart operations, product imagery, and interface presentation.

The observations were documented for comparison with the stated requirements and the predefined test cases.

Not every unexpected behavior is automatically a confirmed defect. Findings should be classified using the expected behavior, supporting evidence, impact, and applicable requirements.

## 8. Limitations

- The exact execution dates and browser details must be taken from the actual test records.
- Some observations require more detailed reproduction information from the existing evidence.
- The permitted character formats for checkout fields are not explicitly defined in REQ-08.
- Root causes have not been established by these exploratory observations alone.

## 9. Conclusion

Exploratory testing supplemented the predefined test cases by identifying additional behaviors worth documenting and evaluating.

The results provide supporting evidence for the project's bug reports and final test summary. All conclusions should remain consistent with the observed behavior and available test evidence.
