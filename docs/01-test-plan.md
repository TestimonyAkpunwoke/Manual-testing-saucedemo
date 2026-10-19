# Test Plan — SauceDemo E-commerce Application

## 1. Document Information

| Field | Details |
|---|---|
| Document ID | QA-SD-TP-001 |
| Project | QA-01 Manual Testing — SauceDemo |
| Version | 1.0 |
| Prepared By | Testimony Akpunwoke |
| Test Type | Manual Functional, Negative, Exploratory and UI Testing |
| Status | Completed — Test Plan and Results Documented |
| Application URL | [https://www.saucedemo.com/](https://www.saucedemo.com/) |
| Date Prepared | 15 October 2026 |
| Test Execution Period | 12–18 October 2026 |

---

## 2. Introduction

### 2.1 Purpose

This test plan defines the scope, objectives, approach, environment, entry and exit criteria, responsibilities, risks, deliverables, and schedule for testing the SauceDemo e-commerce application.

The objective of this project was to evaluate the application's core shopping functionality, verify expected behaviour, identify unexpected results, and produce professional QA documentation suitable for a software testing portfolio.

Testing was conducted from the perspective of an end user. I documented test execution results and exploratory observations, using supporting evidence where available.

### 2.2 Application Overview

SauceDemo is a publicly accessible demonstration e-commerce application that simulates an online shopping experience.

Its main user journey includes:

- Authentication
- Product browsing
- Product sorting
- Shopping cart management
- Checkout information
- Order overview and completion
- Logout and access control

The application provides predefined test accounts with different behaviours, allowing testers to examine normal and abnormal scenarios.

### 2.3 Test Objectives

The objectives of this project were to:

- Verify login, logout, and account access behaviour.
- Evaluate product inventory, product details, images, and sorting.
- Verify adding and removing products from the shopping cart.
- Check cart contents, item details, and displayed prices.
- Test checkout form validation and order completion.
- Evaluate navigation, usability, and visual consistency.
- Identify and document unexpected or potentially defective behaviour.
- Maintain traceability between requirements, test cases, execution results, and reported findings.
- Produce a test summary describing coverage, execution results, findings, limitations, and recommendations.

### 2.4 Application Version

SauceDemo is a shared public demonstration environment. A specific application build or release identifier was not established in the documented test results.

The application should therefore be identified as a **public demo build, with the version not confirmed**.

The recorded test period and environment details provide context for interpreting the results.

---

## 3. Scope

### 3.1 In Scope

The following application areas were included in the testing exercise.

| Application Area | Testing Coverage |
|---|---|
| Authentication | Valid login, invalid credentials, locked-out account behaviour, logout, and access restrictions |
| Inventory | Product visibility, names, descriptions, prices, images, and sorting |
| Shopping Cart | Adding and removing products, cart count, item details, and navigation |
| Checkout | Required-field validation, input handling, checkout progression, order overview, and completion confirmation |
| Navigation and Menu | Navigation links, menu behaviour, logout, and return navigation |
| User Interface | Layout, alignment, text visibility, image rendering, and visual consistency |
| Usability | Clarity of messages, ease of navigation, and obvious interaction problems |
| Error Handling | Unexpected messages, failed actions, inconsistent state, and reproducible functional errors |

The testing exercise covered planned functional scenarios and additional exploratory scenarios. Negative testing and input variation were used where relevant to the available requirements and test cases.

### 3.2 Out of Scope

The following activities were outside the scope of this project:

- Testing real payment gateways or processing actual financial transactions.
- Direct testing of backend services, source code, databases, or internal APIs.
- Comprehensive load, stress, scalability, and performance testing.
- Formal penetration testing or comprehensive security assessments.
- Testing administrative interfaces unavailable through the public application.
- Testing native mobile applications.
- Comprehensive testing of third-party integrations that could not be independently accessed or observed.

Issues discovered incidentally outside the agreed scope may be documented as observations, but such observations do not represent completed testing of those areas.

---

## 4. Test Approach

A risk-based manual testing approach was used to examine the application's main shopping workflows and investigate behaviours that could affect the user experience.

Priority was given to authentication, product selection, cart operations, checkout, and other functionality necessary to complete the shopping journey.

### 4.1 Functional Testing

Functional testing was used to evaluate the application's behaviour against the documented requirements and planned test cases.

The planned testing areas included:

- Logging in with valid and invalid credentials.
- Examining restricted access with the locked-out account.
- Sorting products and checking their displayed order.
- Adding and removing products from the cart.
- Checking cart contents and product information.
- Submitting checkout forms with missing, invalid, and valid information.
- Completing the available checkout flow and checking confirmation behaviour.

The original formal test execution consisted of 43 test cases covering 11 documented requirements. All 43 test cases passed during that recorded execution.

### 4.2 Exploratory Testing

Exploratory testing was conducted after the original planned test execution to investigate behaviours beyond the predefined scenarios.

I explored the application systematically, varied inputs, examined account-specific behaviour, and investigated unexpected results.

Three exploratory sessions produced 14 documented observations across checkout validation, inventory sorting, cart operations, product imagery, visual consistency, and checkout navigation.

These observations were documented separately from the original formal execution results. They were not automatically classified as confirmed defects because some require further reproduction, clarification of expected behaviour, or additional supporting evidence.

### 4.3 Negative and Boundary Testing

Negative testing examined input handling and application behaviour under conditions that could produce validation errors or unexpected results.

The documented scenarios included invalid login attempts, missing or varied checkout inputs, and account-specific behaviour.

Input variations were investigated where relevant to the available fields and documented requirements.

An unexpected result was not automatically treated as a defect. Expected behaviour, reproducibility, applicable requirements, and supporting evidence were considered when documenting findings.

### 4.4 Cross-Browser Compatibility

The initial test plan identified Microsoft Edge and Google Chrome as the intended browsers for selected high-priority compatibility checks.

This was intended to identify obvious browser-specific functional or visual differences rather than provide exhaustive cross-browser certification.

The available execution records establish testing in Microsoft Edge. A completed Google Chrome spot-check result was not established in the documented evidence, so cross-browser compatibility should not be considered fully verified.

### 4.5 Basic Usability and Visual Testing

The testing exercise examined:

- Navigation clarity
- Visibility of information and controls
- Product image rendering
- Product-name alignment
- Sorting behaviour
- Checkout navigation
- General interface consistency

Visual observations were distinguished from confirmed functional defects where expected behaviour was unclear.

### 4.6 Defect Management

Unexpected behaviours were documented for review using the project's exploratory notes and bug-report records.

A useful defect report includes, where applicable:

- Unique defect identifier
- Clear title and description
- Preconditions and test environment
- Test account used
- Steps to reproduce
- Expected result
- Actual result
- Severity and priority, where justified
- Supporting screenshots or other evidence
- Current status and retest outcome

The project distinguishes between an observation, a potential defect, and a confirmed defect. A reported issue should not be considered fixed or closed unless the relevant status is supported by verifiable evidence.

---

## 5. Test Environment

The recorded testing environment was as follows.

| Component | Environment |
|---|---|
| Application | SauceDemo public web application |
| Application URL | [https://www.saucedemo.com/](https://www.saucedemo.com/) |
| Operating System | Windows 11, Version 25H2, OS Build 26200.9711 |
| Browser Used | Microsoft Edge |
| Browser Version | Exact version not established in the final execution summary |
| Device | Desktop computer |
| Network | Internet connection |
| Test Management | GitHub-based project documentation and defect records |
| Test Documentation | Markdown files and test execution spreadsheet |
| Evidence Storage | Project screenshots and supporting files |

### 5.1 Test Accounts

The following predefined accounts were available for the testing exercise.

| Username | Primary Testing Purpose |
|---|---|
| `standard_user` | Normal shopping workflows and checkout input exploration |
| `locked_out_user` | Restricted login behaviour |
| `problem_user` | Investigating inventory, image, sorting, and interaction issues |
| `error_user` | Investigating potential errors during cart and checkout actions |
| `performance_glitch_user` | Investigating unusually slow responses |
| `visual_user` | Examining visual differences and sorting behaviour |

The exploratory findings specifically document the use of `standard_user`, `problem_user`, and `visual_user`.

The account names indicate intended testing scenarios; they do not establish that a defect exists. Each finding must be evaluated independently.

### 5.2 Environment Recording

Relevant execution records and defect reports should identify the following information where available:

- Execution date
- Operating system and browser
- Test account used
- Preconditions and application state
- Steps performed
- Expected and actual results
- Supporting evidence

Because SauceDemo is a shared public environment, its behaviour may change during testing. Recording execution details helps maintain traceability and makes subsequent investigation more reliable.

---

## 6. Entry and Exit Criteria

### 6.1 Entry Criteria

The planned entry criteria were:

- The application is accessible through its public URL.
- The login page loads and the available test accounts can be identified.
- Initial requirements and test-planning documentation are prepared.
- The test environment is available and documented.
- Initial test cases and relevant test data are ready.
- The project repository is available for maintaining documentation and findings.

These criteria define the conditions under which the planned testing activities could begin.

### 6.2 Exit Criteria

The planned exit criteria were:

- Planned test cases have been executed, or exceptions have been documented.
- Test results have been recorded as Pass, Fail, Blocked, or Not Run, as applicable.
- Reported findings have supporting details and evidence where practical.
- Critical-severity defects have been resolved and retested, or unresolved exceptions have been explicitly documented.
- Requirement traceability and test coverage have been reviewed.
- Outstanding issues, limitations, and residual risks have been summarized.
- The final test summary report has been completed.

The exit criteria do not require zero defects. Unresolved findings must be disclosed with their known impact and status.

### 6.3 Recorded Completion Status

The original formal execution covered all 11 documented requirements and 43 planned test cases. All 43 test cases passed during the recorded run.

Subsequent exploratory testing documented 14 observations that may require further investigation or regression coverage.

The formal execution results and exploratory findings are maintained separately so that the original results remain accurate while additional findings can inform future testing.

---

## 7. Roles and Responsibilities

This was an individual QA portfolio project.

**Tester: Testimony Akpunwoke**

My responsibilities included:

- Exploring the application and documenting testable requirements.
- Preparing and maintaining test documentation.
- Designing and executing test cases.
- Performing functional, negative, exploratory, usability, and visual checks.
- Recording actual results and collecting supporting evidence.
- Investigating unexpected behaviour and checking reproducibility.
- Documenting and classifying potential defects.
- Reviewing findings against available requirements.
- Maintaining the Requirements Traceability Matrix.
- Preparing the final test summary and recommendations.

No separate developer, product owner, or independent reviewer was assigned to this project.

I therefore distinguished observed behaviour from assumptions and did not claim that a defect had been fixed unless a verifiable fix was available.

---

## 8. Risks and Mitigation

| Risk | Potential Impact | Mitigation |
|---|---|---|
| Public application changes during testing | Results may become inconsistent or findings may stop reproducing | Record execution dates, environment details, and supporting evidence |
| Limited visibility into the backend | Internal causes of failures cannot be confirmed | Report observable behaviour without claiming an unverified root cause |
| Different test-account behaviours | Results may vary by account or session | Record the account used and reproduce findings where possible |
| Temporary network or service issues | False defect reports or blocked tests | Repeat the test, check availability, and document environmental conditions |
| Undocumented expected behaviour | Incorrect classification of behaviour as a defect | Clarify requirements, record assumptions, and investigate findings |
| Limited testing time | Some scenarios may remain untested | Prioritize high-risk workflows and disclose incomplete coverage |
| Changes to public demo data or configuration | Previously observed behaviour may change | Capture dated evidence and rerun affected tests when necessary |
| Fixes cannot be independently deployed | Retesting may be impossible | Mark fixes as unverified rather than claiming closure |

---

## 9. Deliverables

The project documentation includes the following artefacts.

| Deliverable | Purpose |
|---|---|
| `docs/01-test-plan.md` | Defines the testing scope, approach, environment, criteria, risks, and schedule |
| Requirements documentation | Records numbered, testable requirements and assumptions |
| Test cases and execution records | Documents planned scenarios and their recorded outcomes |
| Requirements Traceability Matrix (RTM) | Maps requirements to test cases and execution results |
| Bug reports | Records findings, reproduction details, expected and actual behaviour, and evidence where available |
| Exploratory testing report | Documents investigation objectives, actions, observations, and findings |
| Screenshot evidence | Provides visual support for observed application behaviour |
| `docs/02-test-summary-report.md` | Summarizes execution results, coverage, findings, and limitations |

These artefacts work together to provide a structured record of the testing activities and their outcomes.

---

## 10. Schedule

The original project schedule was planned over three weeks. The schedule was provisional and could be adjusted based on testing progress, the number of scenarios, and opportunities for retesting.

| Period | Planned Activities | Milestone |
|---|---|---|
| Week 1 | Explore the application, derive requirements, prepare the test plan, design test cases, and prepare the RTM | Requirements and test design documented |
| Week 2 | Execute functional and negative tests, conduct exploratory sessions, perform browser spot checks, capture evidence, and document findings | Initial test execution and findings documented |
| Week 3 | Continue prioritized testing, review coverage, investigate outstanding findings, retest verifiable fixes, and prepare the final summary | Final QA documentation completed |

The recorded testing period was 12–18 October 2026. The available project records establish the original formal execution and exploratory sessions, but do not establish that every originally planned activity, including all browser checks and fix retesting, was completed.

### 10.1 Completion Reporting

The final test summary records:

- Total planned and executed formal test cases.
- Number of formal tests passed and failed.
- Requirement coverage.
- Exploratory observations.
- Outstanding findings and their classification where established.
- Testing limitations and recommendations.

The report distinguishes recorded results from activities or outcomes that have not been independently verified.

---

## 11. Conclusion

This test plan established a structured approach for evaluating the core functionality and user experience of the SauceDemo e-commerce application.

The project covered authentication, inventory, sorting, cart operations, checkout, navigation, and visual behaviour. It also defined the approach for recording test results, maintaining requirements traceability, investigating unexpected behaviour, and documenting findings with supporting evidence.

The original formal execution covered 11 requirements and 43 test cases, with all 43 test cases passing during the recorded run. Subsequent exploratory testing identified 14 additional observations requiring appropriate review and, where necessary, further verification.

Maintaining a distinction between formal execution results and exploratory findings preserves the accuracy of the testing record while allowing new observations to improve future test coverage.

The resulting documentation demonstrates a structured manual QA workflow based on test planning, execution, traceability, exploratory investigation, and evidence-based reporting.

---

## Document History

| Version | Date | Description | Author |
|---|---|---|---|
| 1.0 | 15 October 2026 | Initial test plan | Testimony Akpunwoke |
