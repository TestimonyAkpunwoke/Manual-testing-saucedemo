# Test Summary Report — SauceDemo E-commerce Application

## 1. Document Information

| Field | Details |
|---|---|
| Project | QA-01 Manual Testing — SauceDemo |
| Application | [SauceDemo](https://www.saucedemo.com/) |
| Tester | Testimony Akpunwoke |
| Test period | 12th - 18th of October 2026 |
| Test type | Manual functional, negative, exploratory and UI testing |
| Status | Completed — results documented below |

## 2. Objective

The objective of this testing exercise was to evaluate key e-commerce workflows, identify discrepancies between expected and observed behaviour, and document test results and supporting evidence.

## 3. Scope

The testing covered:

- Login and authentication
- Inventory and product information
- Product sorting
- Cart operations
- Checkout form validation
- Checkout calculations and completion
- Logout and access control
- User interface consistency and usability

## 4. Test Execution Summary

Complete this table using the actual results recorded in the test execution spreadsheet.

| Metric | Result |
|---|---:|
| Total test cases | 54 |
| Executed | 54 |
| Passed | 43 |
| Failed | 11 |
| Blocked | 0 |
| Not run | 0 |

**Execution notes:** [Summarise any relevant constraints or interruptions.]

Do not count exploratory observations as formal test cases unless they were recorded as such in your execution records.

## 5. Requirement Coverage

Requirement coverage was assessed using the Requirements Traceability Matrix (RTM).

- Total requirements: [Actual count]
- Requirements covered by test cases: [Actual count]
- Requirements with recorded execution results: [Actual count]
- Requirements requiring further testing: [Actual count, if applicable]

Refer to the RTM for the mapping between requirements, test cases and execution results.

## 6. Key Findings

The following behaviours were observed during testing. Their final defect status should match the evidence and the corresponding bug reports.

### Checkout validation

- Numeric and punctuation-containing first names were accepted during the observed tests.
- Alphabetic and punctuation-containing postal codes were accepted during the observed tests.
- The last-name field behaved unexpectedly during a test with `problem_user`.

These observations require comparison with explicitly defined validation requirements before they can be classified as confirmed defects.

### Inventory and cart

- Inventory sorting behaved incorrectly in some observed scenarios with `problem_user`.
- Some products could not be removed from the inventory page.
- A product image mismatch was observed: the backpack displayed a dog image.

### Visual consistency and sorting

- Product-name alignment was inconsistent with `visual_user`.
- A–Z and price high-to-low sorting worked in the observed tests.
- Z–A and price low-to-high sorting did not work in the observed tests.
- The checkout button was difficult to locate because of its placement.

See the individual bug reports and linked screenshots for the recorded evidence.

## 7. Defect and Evidence Summary

| Item | Reference |
|---|---|
| Individual defect reports | `bug-reports/` |
| Exploratory testing notes | `docs/03-exploratory-sessions.md` |
| Test cases | `test-cases/` |
| Requirements Traceability Matrix | `test-cases/` |
| Screenshots | `evidence/screenshots/` |

Defect counts and statuses should be taken from the final bug report records. Do not assume every exploratory observation is a confirmed defect.

## 8. Limitations

- Testing was performed manually.
- Results reflect the accounts, workflows and conditions actually tested.
- Untested scenarios cannot be considered verified.
- The findings do not establish the overall quality of the application beyond the scope of this exercise.

## 9. Overall Assessment

**Assessment:** [Complete after reviewing the execution results and outstanding findings.]

Summarise the most important results, unresolved issues and areas requiring further testing.

If making a release recommendation, base it on the actual execution results, defect severity, business impact and applicable acceptance criteria. Do not declare the application ready or unready without sufficient evidence.

## 10. Conclusion

This project documents a structured manual QA exercise covering core e-commerce workflows, requirement traceability, test execution, exploratory observations and defect reporting.

The resulting artefacts demonstrate the ability to plan tests, execute scenarios, record observed behaviour, connect findings to evidence and communicate testing outcomes professionally.

## 11. Supporting Artefacts

- Test plan
- Test cases and execution results
- Requirements Traceability Matrix
- Exploratory testing notes
- Individual bug reports
- Screenshot evidence
