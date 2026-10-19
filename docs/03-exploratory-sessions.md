# Exploratory Testing Report — SauceDemo

## 1. Document Information

| Field | Details |
|---|---|
| Project | SauceDemo Manual QA Portfolio |
| Application | [SauceDemo](https://www.saucedemo.com/) |
| Tester | Testimony Akpunwoke |
| Test Date | 18 October 2026 |
| Browser | Microsoft Edge |
| Operating System | Windows |
| Document Status | Complete |

## 2. Objective

After completing my planned test execution, I conducted exploratory testing on SauceDemo to investigate application behaviour beyond the predefined test cases.

My objective was to identify unexpected behaviour, examine functional and usability concerns, and document findings that could require further investigation.

I focused on checkout information validation, inventory sorting, cart operations, product image accuracy, visual consistency, and checkout navigation.

## 3. Scope

The exploratory testing covered the following areas:

- Checkout information validation
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

**Session ID:** EXP-01  
**Test Account:** `standard_user`  
**Module:** Checkout Information

### Objective

I explored the checkout information form to observe how it handled different input types in the first-name and postal-code fields.

### Observations

| Observation ID | Input Tested | Observed Result |
|---|---|---|
| EXP-01 | Numeric characters in the first-name field | Accepted |
| EXP-02 | Punctuation in the first-name field | Accepted |
| EXP-03 | Alphabetic characters in the postal-code field | Accepted |
| EXP-04 | Punctuation in the postal-code field | Accepted |

### Findings

During this session, I observed that the checkout form accepted numeric and punctuation-only input in the first-name field. It also accepted alphabetic and punctuation-only input in the postal-code field.

These observations raised questions about the validation rules applied to the checkout form.

REQ-08 requires checkout-field validation but does not explicitly define the permitted characters for these fields. I therefore documented the observed behaviour without automatically classifying each observation as a confirmed defect.

### Evidence

Screenshots for this session are maintained in the project's evidence folder.

### Follow-up

- Compare the observations with the intended checkout validation requirements.
- Link the findings to the corresponding entries in the bug register.
- Confirm the expected input rules before classifying the observations as defects.

## 5. Exploratory Session 2 — Inventory and Cart Behaviour

**Session ID:** EXP-02  
**Test Account:** `problem_user`  
**Modules:** Inventory, Sorting, Cart and Checkout Information

### Objective

I explored inventory sorting, cart operations, product imagery, and checkout information handling to identify unexpected behaviour while using the `problem_user` account.

### Observations

| Observation ID | Area Tested | Observed Result |
|---|---|---|
| EXP-05 | Alphabetical and price-based inventory sorting | Sorting did not behave as expected in the observed scenarios. |
| EXP-06 | Removing products from the inventory page | Some products could not be removed as expected. |
| EXP-07 | Checkout last-name field | The field behaved unexpectedly when entering a last name. |
| EXP-08 | Sauce Labs Backpack image | A dog image appeared instead of the expected backpack image. |

### Findings

This session revealed several behaviours that required further investigation.

The inventory sorting behaviour did not appear consistent with the selected sorting options. I also observed difficulties removing some products from the inventory page.

The Sauce Labs Backpack displayed an unrelated dog image, creating a mismatch between the product name and its image. The checkout last-name field also behaved unexpectedly during the observed interaction.

These findings were documented for further investigation. The precise sorting options affected and the exact behaviour of the last-name field should be verified against the original test records and supporting evidence.

### Evidence

Screenshots for this session are maintained in the project's evidence folder.

### Follow-up

- Identify the specific sorting options that did not behave as expected.
- Reproduce the product-removal and last-name-field observations.
- Link each finding to its corresponding bug report.
- Reference related requirements and test cases where applicable.
- Document uncertainty rather than assuming a technical root cause.

## 6. Exploratory Session 3 — Visual Consistency and Sorting

**Session ID:** EXP-03  
**Test Account:** `visual_user`  
**Modules:** Inventory UI, Sorting and Cart / Checkout UI

### Objective

I explored the inventory interface, sorting options, and checkout navigation to identify presentation inconsistencies and unexpected behaviour while using the `visual_user` account.

### Observations

| Observation ID | Area Tested | Observed Result |
|---|---|---|
| EXP-09 | Product-name alignment | Some product names appeared left-aligned while others appeared right-aligned. |
| EXP-10 | Name sorting: A–Z | Worked correctly. |
| EXP-11 | Name sorting: Z–A | Did not work correctly. |
| EXP-12 | Price sorting: high to low | Worked correctly. |
| EXP-13 | Price sorting: low to high | Did not work correctly. |
| EXP-14 | Checkout button placement | The button appeared near the upper-right area and was difficult to locate. |

### Findings

The session revealed inconsistencies in product-name alignment and sorting behaviour.

The A–Z and price high-to-low sorting options worked correctly during my observations. However, the Z–A and price low-to-high options did not behave as expected.

I also observed that the Checkout button appeared near the upper-right area of the cart page and was difficult to locate.

I documented both the successful and unsuccessful sorting observations to preserve an accurate record of the application's behaviour. The button-placement observation was recorded as a usability concern rather than automatically treated as a confirmed defect.

### Evidence

Screenshots for this session are maintained in the project's evidence folder.

### Follow-up

- Link the sorting observations to the corresponding bug reports and test cases.
- Preserve the successful sorting results as evidence of the behaviours that worked during this session.
- Reproduce the unsuccessful sorting scenarios to confirm their consistency.
- Assess the checkout button's placement against the intended interface design and usability criteria.

## 7. Summary of Exploratory Findings

Across the three sessions, I documented 14 observations involving checkout validation, inventory sorting, cart operations, product imagery, and interface presentation.

| Area | Observations | Summary |
|---|---:|---|
| Checkout input validation | 4 | Different input types were accepted; validation rules require clarification. |
| Inventory and cart behaviour | 4 | Sorting, product removal, checkout field behaviour, and product imagery raised concerns. |
| Visual consistency and sorting | 6 | Alignment inconsistencies, successful and unsuccessful sorting options, and a checkout usability concern were recorded. |
| **Total** | **14** | **Observations documented for review and follow-up.** |

The 14 observations are not necessarily equivalent to 14 confirmed defects. Some findings may require clarification, further reproduction, or additional evidence before they can be classified conclusively.

The findings were documented in the project's bug register where applicable.

## 8. Relationship to Planned Test Execution

I completed the planned test execution before conducting these exploratory sessions.

The original execution covered 43 planned test cases, all of which passed during that recorded run.

The exploratory sessions were conducted separately and revealed additional behaviours that were not identified during the original execution.

I retained the original execution results as a record of what occurred during those test runs. The exploratory findings were documented separately so they could be investigated and used to improve future test coverage.

Where an exploratory finding relates to an existing requirement, the relevant test case and Requirements Traceability Matrix (RTM) should be reviewed. Additional regression test cases can be introduced where necessary.

This approach preserves the original execution history while allowing the test suite to evolve based on new findings.

## 9. Limitations

The following limitations apply to this report:

- Some findings may require additional reproduction details from the original test records.
- The permitted character formats for checkout fields are not explicitly defined in REQ-08.
- The exact sorting options affected under `problem_user` should be interpreted using the supporting evidence.
- The precise behaviour of the checkout last-name field may require further verification.
- The checkout button placement was recorded as a usability concern; confirming it as a defect requires an applicable design or usability criterion.
- Root causes were not established by these exploratory observations alone.

## 10. Conclusion

Conducting exploratory testing allowed me to investigate SauceDemo beyond the predefined test cases and document additional behaviours that warranted attention.

The sessions revealed observations involving checkout validation, inventory sorting, cart operations, product image accuracy, visual consistency, and checkout navigation.

The exercise demonstrated the importance of distinguishing between a test observation, a potential defect, and a confirmed defect. An unexpected result should be evaluated against expected behaviour, available requirements, reproducibility, and supporting evidence before a definitive conclusion is reached.

I documented these findings to support the project's bug reports, identify opportunities to improve test coverage, and inform future regression testing.

Overall, exploratory testing complemented my planned test execution by helping me investigate scenarios beyond the original test cases and identify areas requiring further verification.

## 11. Supporting Project Artefacts

The following artefacts support this report:

- **Requirements:** Documented application requirements.
- **Test Cases:** Predefined test scenarios.
- **Execution Results:** Results from the original test execution.
- **Requirements Traceability Matrix (RTM):** Mapping between requirements and test cases.
- **Bug Register:** Central record of reported findings.
- **Individual Bug Reports:** Detailed reproduction steps, expected and actual results, and impact where applicable.
- **Screenshots and Evidence:** Supporting evidence captured during testing.

Together, these artefacts provide a record of the testing activities, observations, and findings from the SauceDemo Manual QA Portfolio project.
