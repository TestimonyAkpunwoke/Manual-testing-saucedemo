# Test Plan — Sauce Demo E-commerce Application

| Document Information | Details                                                  |
| -------------------- | -------------------------------------------------------- |
| Document ID          | QA-SD-TP-001                                             |
| Project              | Sauce Demo Manual QA Portfolio                           |
| Version              | 1.0                                                      |
| Prepared by          | Testimony Akpunwoke                                      |
| Test Type            | Manual Software Testing                                  |
| Status               | Draft — testing in progress                              |
| Application URL      | [https://www.saucedemo.com/](https://www.saucedemo.com/) |
| Date Prepared        | 15 October 2026                                          |
| Test Execution Date  | To be recorded during execution                          |

---

## 1. Introduction

### 1.1 Purpose

This test plan defines the scope, objectives, approach, environment, entry and exit criteria, responsibilities, risks, deliverables, and schedule for testing the Sauce Demo e-commerce application.

The project aims to evaluate the application's core shopping functionality, identify and document reproducible defects, verify expected behaviour, and produce professional QA documentation suitable for a software testing portfolio.

Testing will be conducted from the perspective of an end user. Findings will be supported by clear reproduction steps and evidence wherever possible.

### 1.2 Application Overview

Sauce Demo is a publicly accessible demonstration e-commerce application that simulates an online shopping experience. Its main user journey includes authentication, product browsing, shopping cart management, and checkout.

The application provides predefined test accounts that exhibit different behaviours, enabling the tester to investigate normal and abnormal scenarios.

### 1.3 Test Objectives

The objectives of this project are to:

- Verify login, logout, and account access behaviour.
- Evaluate product inventory, product details, images, and sorting.
- Verify adding and removing products from the shopping cart.
- Check cart contents, item details, and displayed prices.
- Test checkout form validation and order completion.
- Evaluate navigation, usability, and visual consistency.
- Identify, document, and classify reproducible defects.
- Maintain traceability between requirements, test cases, and reported defects.
- Produce a final test summary describing coverage, findings, outstanding defects, and recommendations.

### 1.4 Application Version

Sauce Demo is a shared public demonstration environment. A specific build or release identifier will be recorded if one is available.

If no version is displayed, the test record will state **"Public demo build — version not displayed."** The execution date and environment details will be recorded to help identify the version of the application that was tested.


## 2. Scope

### 2.1 In Scope

| Application Area    | Testing Coverage                                                                                             |
| ------------------- | ------------------------------------------------------------------------------------------------------------ |
| Authentication      | Valid login, invalid credentials, locked-out account behaviour, logout, and access restrictions              |
| Inventory           | Product visibility, product names, descriptions, prices, images, and sorting                                 |
| Shopping Cart       | Adding and removing products, cart count, item details, and navigation                                       |
| Checkout            | Required-field validation, invalid inputs, checkout progression, order overview, and completion confirmation |
| Navigation and Menu | Navigation links, menu opening and closing, logout, and return navigation                                    |
| User Interface      | Layout, alignment, text visibility, image rendering, and visual consistency                                  |
| Usability           | Clarity of messages, ease of navigation, and obvious interaction problems                                    |
| Error Handling      | Unexpected messages, failed actions, inconsistent state, and reproducible functional errors                  |

Testing will cover successful user journeys and negative scenarios, including invalid credentials, missing required fields, and restricted account access.

### 2.2 Out of Scope

The following activities are excluded:

- Testing real payment gateways or processing actual financial transactions.
- Direct testing of backend services, source code, databases, or internal APIs.
- Comprehensive load, stress, scalability, and performance testing.
- Formal penetration testing or comprehensive security assessments.
- Testing administrative interfaces not available through the public application.
- Testing native mobile applications.
- Comprehensive testing of third-party integrations that cannot be independently accessed or observed.

Issues discovered incidentally outside the agreed scope may be documented as observations, but they will not be represented as completed testing of those areas.

## 3. Test Approach

A risk-based manual testing approach will be used. Priority will be given to core shopping journeys and features whose failure could prevent users from accessing the application, selecting products, or completing checkout.

### 3.1 Functional Testing

Functional testing will verify whether the application behaves according to documented requirements.

Activities include:

- Logging in with valid and invalid credentials.
- Testing restricted access with the locked-out account.
- Sorting products and checking their displayed order.
- Adding and removing products from the cart.
- Checking cart contents and product information.
- Submitting checkout forms with missing, invalid, and valid information.
- Completing the available checkout flow and checking the confirmation.

### 3.2 Exploratory Testing

Exploratory testing will be used to investigate behaviors not fully covered by predefined test cases.

The tester will explore the application systematically, vary inputs, follow different navigation paths, and investigate unexpected results.

Each exploratory session will record its objective, areas explored, actions performed, observations, and any defects discovered.

### 3.3 Negative and Boundary Testing

Negative testing will examine invalid inputs and unsupported actions, such as incorrect login credentials, missing required checkout fields, and restricted account access.

Boundary checks will be performed where relevant to the available fields and documented requirements.

A result will not be classified as a defect solely because it is unexpected; the expected behaviour must be established and the finding investigated.

### 3.4 Cross-Browser Spot Checks

Selected high-priority workflows will be checked in Microsoft Edge and Google Chrome.

The purpose is to identify obvious browser-specific functional or visual differences. This is a limited compatibility check rather than exhaustive cross-browser certification.

### 3.5 Basic Usability and Visual Testing

The tester will evaluate navigation clarity, information visibility, control usability, image rendering, alignment, and layout consistency throughout the main shopping journey.

Visual observations will be distinguished from confirmed functional defects when the expected behaviour is unclear.

### 3.6 Defect Management

Confirmed defects will be recorded in GitHub Issues and tracked through the GitHub Project board.

Each defect report will include, where applicable:

- Unique defect identifier.
- Clear title and description.
- Preconditions and test environment.
- Steps to reproduce.
- Expected result.
- Actual result.
- Severity and relevant labels.
- Supporting screenshots or other evidence.
- Current status and retest outcome.

Only reproducible, evidence-supported issues will be reported as confirmed defects.

---

## 4. Test Environment

Testing will be performed using the following environment.

| Component          | Environment                                                         |
| ------------------ | ------------------------------------------------------------------- |
| Application        | Sauce Demo public web application                                   |
| Application URL    | [https://www.saucedemo.com/](https://www.saucedemo.com/)            |
| Operating System   | Windows 11, Version 25H2, OS Build 26200.9711                       |
| Browser 1          | Microsoft Edge, Version 155.0.4283.45 (Official build) (64-bit)     |
| Browser 2          | Google Chrome, Version 155.0.8059.40 (Official Build) (64-bit)      |
| Device             | Desktop computer                                                    |
| Network            | Internet connection                                                 |
| Test Management    | GitHub Issues and GitHub Projects                                   |
| Test Documentation | Markdown files stored in the project repository                     |
| Evidence Storage   | Relevant screenshots and supporting files in the project repository |

### 4.1 Test Accounts

The following predefined accounts will be used where relevant:

| Username                  | Primary Testing Purpose                                     |
| ------------------------- | ----------------------------------------------------------- |
| `standard_user`           | Normal shopping workflows                                   |
| `locked_out_user`         | Restricted login behaviour                                  |
| `problem_user`            | Potential inventory, image, sorting, and interaction issues |
| `error_user`              | Potential errors during cart and checkout actions           |
| `performance_glitch_user` | Observing unusually slow responses                          |
| `visual_user`             | Examining visual differences                                |

The shared demo password will be obtained from the application's login page and used as instructed there.

The account names indicate intended testing scenarios; they do not establish that a defect exists. Each finding must be independently investigated and verified.

### 4.2 Environment Recording

For relevant test executions and defect reports, the tester will record:

- Execution date and time.
- Operating system and browser version.
- Test account used.
- Preconditions and relevant application state.
- Steps performed and actual results.
- Supporting evidence where available.

Because Sauce Demo is a shared public environment, its behavior may change during the project. Recording the environment and execution date will help make findings traceable.

---

## 5. Entry and Exit Criteria

### 5.1 Entry Criteria

Testing may begin when:

- The application is accessible through its public URL.
- The login page loads and the available test accounts can be identified.
- The initial requirements document and test plan are prepared.
- The test environment is available and documented.
- Initial test cases and relevant test data are ready.
- The GitHub repository is available for documentation and defect tracking.

If an entry criterion is not met, the limitation will be recorded before testing proceeds.

### 5.2 Exit Criteria

The testing engagement will be considered complete when:

- All planned high-priority test cases have been executed, or exceptions have been documented.
- Test results have been recorded as Pass, Fail, Blocked, or Not Run.
- Confirmed defects have documented reports and supporting evidence where practical.
- Critical-severity defects have been resolved and successfully retested, or any unresolved exception has been explicitly documented.
- Requirements traceability and test coverage have been reviewed.
- Outstanding major and minor defects, limitations, and residual risks have been summarized.
- The final test summary report has been completed.

The exit criteria do not require zero defects. All unresolved issues must be disclosed with their impact and current status.

---

## 6. Roles and Responsibilities

This is an individual QA portfolio project.

**Tester: Testimony Akpunwoke**

The tester is responsible for:

- Exploring the application and deriving testable requirements.
- Preparing and maintaining test documentation.
- Designing and executing test cases.
- Performing functional, negative, exploratory, usability, and visual checks.
- Recording actual results and collecting evidence.
- Investigating unexpected behavior and checking reproducibility.
- Reporting, classifying, and tracking defects.
- Retesting fixes when a verifiable fix becomes available.
- Maintaining the Requirements Traceability Matrix.
- Preparing the final test summary and recommendations.

No separate developer, product owner, or independent reviewer is assigned to this project. The tester will distinguish observed facts from assumptions and will not claim that a fix has been implemented unless it can be verified.

---

## 7. Risks and Mitigation

| Risk                                         | Potential Impact                                                | Mitigation                                                                 |
| -------------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Public application changes during testing    | Results may become inconsistent or defects may stop reproducing | Record execution dates, environment details, and supporting evidence       |
| Limited visibility into the backend          | Internal causes of failures cannot be confirmed                 | Report observable behaviour without claiming an unverified root cause      |
| Different test-account behaviours            | Results may vary by account or session                          | Record the account used and reproduce findings where possible              |
| Temporary network or service issues          | False defect reports or blocked tests                           | Repeat the test, check availability, and document environmental conditions |
| Undocumented expected behaviour              | Incorrect classification of behaviour as a defect               | Derive explicit requirements, record assumptions, and investigate findings |
| Limited testing time                         | Some scenarios may remain untested                              | Prioritize high-risk workflows and disclose incomplete coverage            |
| Changes to public demo data or configuration | Previously observed behaviour may change                        | Capture dated evidence and rerun affected tests when necessary             |
| Fixes cannot be independently deployed       | Retesting may be impossible                                     | Mark tests as blocked or fixes as unverified rather than claiming closure  |

---

## 8. Deliverables

The following artifacts will be maintained in the GitHub repository:

| Deliverable                            | Purpose                                                                          |
| -------------------------------------- | -------------------------------------------------------------------------------- |
| `docs/01-test-plan.md`                 | Defines the testing scope, approach, environment, criteria, risks, and schedule  |
| `docs/02-requirements.md`              | Records numbered, testable requirements and assumptions                          |
| Test case document                     | Records preconditions, steps, test data, expected results, and execution results |
| Requirements Traceability Matrix (RTM) | Maps requirements to test cases and their execution status                       |
| GitHub Issues                          | Stores individual defect reports with reproduction steps, severity, and evidence |
| GitHub Project board                   | Tracks defects through New, Confirmed, Fixed, Retest, and Closed                 |
| Exploratory session notes              | Records investigation goals, actions, observations, and discoveries              |
| Test evidence                          | Contains relevant screenshots and other supporting material                      |
| Test summary report                    | Summarizes execution, coverage, defects, limitations, and recommendations        |

Exact filenames for the test case document, traceability matrix, session notes, and summary report will be established as the repository structure is finalized.

---

## 9. Schedule

The project is planned over three weeks. The schedule is provisional and may be adjusted based on testing progress, the number of scenarios, and retesting opportunities.

| Week   | Activities                                                                                                                             | Milestone                                           |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| Week 1 | Explore the application, derive requirements, finalize the test plan, design test cases, and prepare the traceability matrix           | Requirements and test design documented             |
| Week 2 | Execute functional and negative tests, conduct exploratory sessions, perform browser spot checks, capture evidence, and report defects | Initial test execution and defect reports completed |
| Week 3 | Continue prioritized testing, review coverage, retest verifiable fixes, investigate outstanding findings, and prepare the test summary | Final QA documentation and test summary completed   |

### 9.1 Completion Reporting

At the end of Week 3, the test summary will report:

- Total test cases planned and executed.
- Number of tests passed, failed, blocked, and not run.
- Requirements and test coverage.
- Confirmed defects grouped by severity.
- Outstanding issues and residual risks.
- Testing limitations and recommendations.

No completion status will be reported until the corresponding activities have actually been performed.

---

## Document History

| Version | Date            | Description       | Author              |
| ------- | --------------- | ----------------- | ------------------- |
| 1.0     | 15 October 2026 | Initial test plan | Testimony Akpunwoke |

