# Test Summary Report — SauceDemo E-commerce Application

## 1. Document Information

| Field | Details |
|---|---|
| Project | QA-01 Manual Testing — SauceDemo |
| Application | [SauceDemo](https://www.saucedemo.com/) |
| Tester | Testimony Akpunwoke |
| Test Period | 12–18 October 2026 |
| Test Type | Manual Functional, Negative, Exploratory and UI Testing |
| Status | Completed — Results Documented |

## 2. Objective

The objective of this testing exercise was to evaluate key e-commerce workflows in SauceDemo, verify application behaviour against documented requirements, identify discrepancies between expected and observed results, and record test outcomes with supporting evidence.

The exercise also included exploratory testing to investigate scenarios beyond the original planned test cases and identify additional behaviours requiring further review.

## 3. Scope

The testing activities covered the following areas:

- Login and authentication
- Inventory and product information
- Product sorting
- Cart operations
- Checkout form validation
- Checkout calculations and completion
- Logout and access control
- User interface consistency and usability

Testing was performed using the `standard_user`, `problem_user`, and `visual_user` accounts where applicable.

## 4. Test Execution Summary

The original planned test execution consisted of 43 test cases covering 11 documented requirements.

| Metric | Result |
|---|---:|
| Total documented requirements | 11 |
| Original planned test cases | 43 |
| Original executed test cases | 43 |
| Original passed test cases | 43 |
| Original failed test cases | 0 |
| Additional exploratory observations | 14 |

**Original execution pass rate: 100%**

The pass rate is calculated from the original formal test execution: 43 passed test cases out of 43 executed test cases.

The 14 exploratory observations are documented separately from the original execution results. They are not included in the formal test execution totals because they were recorded as exploratory findings rather than as additional executed formal test cases.

The original results represent the behaviour observed during that particular test run. The subsequent exploratory findings are recorded separately for investigation and potential regression coverage.

## 5. Requirement Coverage

Requirement coverage was assessed using the Requirements Traceability Matrix (RTM).

| Coverage Metric | Result |
|---|---:|
| Total documented requirements | 11 |
| Requirements covered by test cases | 11 |
| Requirements with recorded execution results | 11 |
| Requirements without recorded execution results | 0 |

All 11 documented requirements were mapped to test cases and had recorded execution results in the original test execution.

The RTM provides traceability between requirements, test cases, and their execution results.

Although all documented requirements were covered during the original planned execution, the additional exploratory observations identified behaviours that may warrant further testing and clarification of expected behaviour.

## 6. Key Findings

Exploratory testing identified additional behaviours across checkout validation, inventory operations, sorting, product imagery, and interface presentation.

These findings are documented separately from the original formal test execution.

### 6.1 Checkout Validation

During exploratory testing with `standard_user`, I observed that:

- Numeric characters were accepted in the first-name field.
- Punctuation was accepted in the first-name field.
- Alphabetic characters were accepted in the postal-code field.
- Punctuation was accepted in the postal-code field.

During a separate session with `problem_user`, the last-name field also behaved unexpectedly.

These observations raised questions about the validation rules applied to checkout information. However, the documented requirement does not fully specify the permitted input formats for each field. I therefore recorded the observations for further investigation rather than automatically classifying every instance as a confirmed defect.

### 6.2 Inventory and Cart Behaviour

During exploratory testing with `problem_user`, I observed that:

- Inventory sorting did not behave as expected in some scenarios.
- Some products could not be removed from the inventory page as expected.
- The Sauce Labs Backpack displayed a dog image instead of the expected product image.

These observations highlighted potential functional and product-presentation issues requiring further investigation and supporting evidence.

### 6.3 Visual Consistency and Sorting

During exploratory testing with `visual_user`, I observed that:

- Some product names appeared inconsistently aligned.
- A–Z name sorting worked correctly in the observed test.
- Z–A name sorting did not work as expected.
- Price sorting from high to low worked correctly in the observed test.
- Price sorting from low to high did not work as expected.
- The Checkout button appeared near the upper-right area and was difficult to locate.

I documented both successful and unsuccessful sorting behaviour to preserve an accurate record of the observations. The checkout button placement was recorded as a usability concern; confirming it as a defect would require comparison with the intended interface design or applicable usability criteria.

### 6.4 Interpretation of Findings

The exploratory findings demonstrate why a successful planned test run does not necessarily establish that every aspect of an application behaves as expected under all conditions.

The findings must be assessed against expected behaviour, reproducibility, applicable requirements, and available evidence before their final defect status is determined.

Individual findings and their supporting evidence are maintained in the project's bug reports and exploratory testing documentation.

## 7. Defect and Evidence Summary

The following project artefacts support the testing results and exploratory findings.

| Artefact | Location |
|---|---|
| Test plan | Project documentation |
| Test cases | `test-cases/` |
| Test execution results | Test execution spreadsheet |
| Requirements Traceability Matrix | `test-cases/` |
| Exploratory testing report | `docs/03-exploratory-sessions.md` |
| Individual bug reports | `bug-reports/` |
| Screenshot evidence | `evidence/screenshots/` |

The exploratory report documents 14 observations across three sessions. These observations should not automatically be treated as 14 confirmed defects.

The individual bug reports provide the detailed records for reported findings, including reproduction steps, expected and actual behaviour, environment or test account, and supporting evidence where available.

A final confirmed-defect count is not stated in this report because it should reflect the final classification and status of the individual bug records.

## 8. Limitations

The following limitations apply to this testing exercise:

- Testing was performed manually.
- Results reflect the accounts, workflows, and conditions actually tested.
- Untested scenarios cannot be considered verified.
- Some exploratory observations require further reproduction or clarification of expected behaviour.
- The documented checkout validation requirements do not fully specify all permitted input formats.
- The exact behaviour of some sorting and checkout-field scenarios requires reference to the supporting evidence.
- Root causes were not established by the exploratory observations alone.
- The findings do not establish the overall quality of the application beyond the scope of this exercise.

## 9. Overall Assessment

**Assessment: The original planned test execution passed, with additional exploratory findings requiring review.**

The original formal test execution achieved a 100% pass rate, with all 43 executed test cases passing across the 11 documented requirements.

However, subsequent exploratory testing identified 14 observations involving checkout input validation, inventory sorting, cart operations, product imagery, visual consistency, and checkout navigation.

These results are not contradictory. The formal test cases passed under their recorded execution conditions, while exploratory testing investigated additional scenarios and account-specific behaviour outside the original execution results.

The overall assessment is therefore that the planned test execution was successful, but the exploratory findings should be reviewed before drawing broader conclusions about the application's behaviour.

The evidence supports reporting the formal execution results as passed while maintaining the exploratory findings as separate items requiring appropriate verification and classification.

## 10. Conclusion

This project documents a structured manual QA exercise covering core e-commerce workflows, requirements traceability, test execution, exploratory testing, and defect reporting.

I executed 43 planned test cases against 11 documented requirements, with all 43 test cases passing during the original recorded execution. I then conducted exploratory testing to investigate additional scenarios and documented 14 observations requiring review or further verification.

The exercise demonstrates my approach to organising requirements, executing test cases, recording results, investigating unexpected behaviour, maintaining traceability, and communicating findings through structured testing documentation.

It also reinforced the importance of distinguishing between a successful test execution, an unexpected observation, a potential defect, and a confirmed defect. Each finding must be assessed against expected behaviour and supporting evidence before a definitive conclusion is reached.

Overall, the project provides a documented example of manual functional testing complemented by exploratory testing and evidence-based reporting.

## 11. Supporting Artefacts

The following artefacts form part of this QA portfolio project:

- **Test Plan:** Defines the testing scope, objectives, and approach.
- **Test Cases and Execution Results:** Records the planned scenarios and the outcomes from the original execution.
- **Requirements Traceability Matrix (RTM):** Maps documented requirements to test cases and execution results.
- **Exploratory Testing Report:** Documents additional observations from exploratory sessions.
- **Individual Bug Reports:** Records reported findings and their supporting details.
- **Screenshot Evidence:** Provides visual support for observed application behaviour.

Together, these artefacts document the testing process, preserve the original execution results, and provide a structured record of the additional findings identified during exploratory testing.
