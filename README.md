# SauceDemo E-commerce Application — Manual QA Testing

## Project Overview

This project documents a manual Quality Assurance (QA) testing exercise on the [SauceDemo](https://www.saucedemo.com/) e-commerce application.

The goal was to evaluate core shopping workflows, verify expected behaviour, explore selected user scenarios, document observed discrepancies, and organise test evidence in a professional QA portfolio.

## Objectives

- Develop a structured test plan.
- Design test cases based on defined requirements.
- Map requirements to test cases using a Requirements Traceability Matrix (RTM).
- Execute test scenarios and record actual results.
- Perform exploratory testing.
- Document observed issues with supporting evidence.
- Summarise testing outcomes and limitations.

## Scope of Testing

The testing covered the following areas:

- Login and authentication
- Product inventory and product information
- Product sorting
- Cart operations
- Checkout form validation
- Checkout calculations and completion
- Logout and access control
- User interface consistency and usability

## Test Approach

The project combined planned manual test execution with exploratory testing.

Test accounts used during the exercise included `standard_user`, `problem_user`, and `visual_user`.

Testing findings were recorded against observed application behaviour. Any final defect classification should be interpreted alongside the documented requirements, expected results, and supporting evidence.

## Repository Structure

```text
qa-01-manual-testing-saucedemo/
├── README.md
├── .gitignore
├── docs/
│   ├── 01-test-plan.md
│   ├── 02-test-summary-report.md
│   └── 03-exploratory-sessions.md
├── test-cases/
│   ├── test-cases.xlsx
│   └── traceability-matrix.xlsx
├── bug-reports/
│   └── individual bug reports
└── evidence/
    └── screenshots/
```

*This structure describes the intended organisation. Update the names above to match the files actually present in the repository.*

## Test Artefacts

| Artefact | Purpose |
|---|---|
| [Test Plan](docs/01-test-plan.md) | Defines the testing objectives, scope and approach |
| [Test Summary Report](docs/02-test-summary-report.md) | Summarises execution results, findings and limitations |
| [Exploratory Testing Notes](docs/03-exploratory-sessions.md) | Records exploratory sessions and observations |
| Test Cases | Contains test scenarios, steps, expected results and recorded outcomes |
| Requirements Traceability Matrix | Maps requirements to associated test cases |
| Bug Reports | Documents individual observed issues |
| Screenshot Evidence | Supports relevant observations and bug reports |

## Key Observations

During testing, observations included:

- Product image mismatches.
- Inconsistent product sorting behaviour in selected scenarios.
- Unexpected behaviour in selected checkout form fields.
- Product removal difficulties in selected scenarios.
- Inconsistent product-name alignment and checkout button discoverability.

These are observations from the tested scenarios, not a claim that every issue affects every user account or every application workflow.

Refer to the individual reports and screenshot evidence for the specific conditions observed.

## Tools and Technologies

- SauceDemo — application under test
- Google Sheets — test case design, traceability and execution records
- Microsoft Excel (`.xlsx`) — exported spreadsheet artefacts
- GitHub — version control and portfolio documentation
- Markdown — test plans, exploratory notes, reports and bug documentation
- Browser — manual interaction and observation

## Results

The final test execution counts, requirement coverage, and defect statuses are recorded in the [Test Summary Report](docs/02-test-summary-report.md).

**Execution status:** [Add the verified summary from your completed test records.]

## Limitations

- Testing was performed manually.
- Findings apply to the scenarios and accounts actually tested.
- Untested scenarios are not considered verified.
- The project does not claim exhaustive application coverage.

## Learning Outcomes

This project demonstrates practical work in:

- Test planning and test case design
- Requirements traceability
- Manual test execution
- Exploratory testing
- Defect reporting and evidence collection
- Test result documentation
- QA artefact organisation and version control

## Author

**Testimony Akpunwoke**

GitHub: [TestimonyAkpunwoke](https://github.com/TestimonyAkpunwoke)

---

This project is a learning and portfolio exercise demonstrating a structured manual QA workflow.
