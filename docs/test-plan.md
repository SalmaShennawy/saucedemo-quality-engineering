# SauceDemo – Software Test Plan

| Document Attribute | Details |
|---|---|
| Document ID | SDQA-TP-001 |
| Project Name | SauceDemo Quality Engineering |
| Application Under Test | SauceDemo |
| Application URL | https://www.saucedemo.com/ |
| Document Version | 1.0 |
| Document Status | Draft |
| Testing Approach | Manual and Automated |
| Prepared By | QA Engineer |
| Last Updated | 2026-11-13 |

---

## 1. Introduction

### 1.1 Purpose

This document defines the overall testing approach, scope, objectives, resources, activities, and acceptance criteria for the SauceDemo Quality Engineering project.

The purpose of this test plan is to establish a structured testing process that validates the functional behavior, usability, reliability, and quality of the SauceDemo e-commerce application.

The project demonstrates the application of professional Quality Assurance practices throughout the Software Testing Life Cycle (STLC), combining manual testing with automated browser testing.

### 1.2 Project Overview

SauceDemo is a demonstration e-commerce web application that simulates a simplified online shopping experience.

Users can authenticate, browse products, view product details, manage shopping carts, provide checkout information, and complete simulated orders.

This project will validate the application's primary business workflows and identify potential functional and usability issues.

### 1.3 Testing Objectives

The main testing objectives are:

1. Validate the application's core functional requirements.
2. Verify authentication and authorization behavior.
3. Validate product inventory and sorting functionality.
4. Verify shopping cart operations and product management.
5. Validate checkout workflows and input validation.
6. Verify order calculations and confirmation behavior.
7. Identify, document, and report application defects.
8. Establish traceability between requirements and test cases.
9. Develop a maintainable Playwright automation framework.
10. Integrate automated regression testing into a CI/CD pipeline.

---

## 2. Test Scope

### 2.1 In-Scope Features

The following application modules are included in the testing scope.

| Module | Features Under Test |
|---|---|
| Authentication | Login, credential validation, locked accounts, error handling |
| Product Inventory | Product listing, product information, sorting, images |
| Product Details | Product information, navigation, add-to-cart functionality |
| Shopping Cart | Add products, remove products, cart contents, cart badge |
| Checkout Information | Customer information, mandatory fields, input validation |
| Order Completion | Order summary, item total, tax, final amount, confirmation |
| Navigation & Session | Navigation menu, logout, application state management |

### 2.2 Out-of-Scope Features

The following activities are excluded from the current testing scope:

- Real payment gateway integration.
- Actual financial transactions.
- Customer registration and account creation.
- Production database validation.
- Third-party payment provider testing.
- Backend infrastructure and server administration.
- Load and stress testing of production infrastructure.
- Security penetration testing.
- Mobile native application testing.

These exclusions reflect the capabilities and intended use of the demonstration application.

---

## 3. Test Strategy

### 3.1 Testing Levels

The project will primarily focus on application-level testing.

| Testing Level | Description | Applicable |
|---|---|---|
| Unit Testing | Validation of individual code components | No – outside project access |
| Integration Testing | Validation of integrated application components | Limited, where observable |
| System Testing | Validation of complete application workflows | Yes |
| Acceptance Testing | Validation of user-oriented business workflows | Yes |

### 3.2 Testing Types

The following testing types will be performed:

**Functional Testing**
- Validate application features against expected behavior.
- Verify business workflows and user interactions.
- Validate application responses to valid and invalid inputs.

**Negative Testing**
- Test invalid credentials.
- Submit incomplete checkout information.
- Verify appropriate error handling.
- Validate restricted access scenarios.

**UI Testing**
- Verify page elements and product information.
- Validate button and navigation behavior.
- Verify product images and displayed information.

**End-to-End Testing**
- Execute complete shopping journeys.
- Validate login, product selection, cart management, checkout, and order confirmation.

**Regression Testing**
- Re-execute previously validated scenarios after changes.
- Verify that existing functionality remains stable.

**Exploratory Testing**
- Investigate application behavior outside predefined test scenarios.
- Explore unusual user interactions and edge cases.

**Basic Accessibility Testing**
- Inspect keyboard navigation, focus behavior, labels, and visible interaction states.
- This is a limited accessibility assessment, not a formal WCAG conformance audit.

### 3.3 Test Design Techniques

The following ISTQB-aligned techniques will be used:

| Technique | Application |
|---|---|
| Equivalence Partitioning | Valid and invalid login inputs |
| Boundary Value Analysis | Input field validation and limits |
| Decision Table Testing | Authentication and checkout validation rules |
| State Transition Testing | Cart and application state changes |
| Use Case Testing | Complete shopping workflows |
| Exploratory Testing | Unexpected user behavior |

### 3.4 Testing Approach

Testing will be performed in two main phases.

**Phase 1: Manual Testing**

- Analyze application functionality.
- Identify test scenarios.
- Design detailed test cases.
- Prepare test data.
- Execute test cases.
- Record actual results.
- Report and track defects.
- Prepare test execution reports.

**Phase 2: Automation Testing**

- Design a reusable Playwright framework.
- Implement the Page Object Model.
- Automate selected manual test cases.
- Implement reusable fixtures and test data.
- Execute tests across supported browsers.
- Generate automated execution reports.
- Integrate execution with GitHub Actions.

---

## 4. Test Environment

### 4.1 Application Environment

| Attribute | Configuration |
|---|---|
| Application | SauceDemo |
| Environment | Public demonstration environment |
| URL | https://www.saucedemo.com/ |
| Application Type | Web Application |
| Execution Mode | Manual and Automated |
| Primary Browser | Google Chrome |
| Additional Browsers | Firefox and WebKit |

Browser coverage will depend on availability and compatibility during execution.

### 4.2 Automation Environment

| Component | Technology |
|---|---|
| Programming Language | Python 3.12+ |
| Automation Tool | Playwright |
| Test Framework | Pytest |
| Design Pattern | Page Object Model |
| Test Data | JSON |
| Reporting | Allure |
| Version Control | Git |
| Repository | GitHub |
| CI/CD | GitHub Actions |

### 4.3 Test Accounts

The following demonstration accounts will be used.

| Username | Purpose |
|---|---|
| standard_user | Standard functional testing |
| locked_out_user | Authentication negative testing |
| problem_user | Application anomaly testing |
| performance_glitch_user | Response-time behavior exploration |
| error_user | Error-handling exploration |
| visual_user | Visual behavior testing |

**Password:** `secret_sauce`

These are publicly documented demonstration credentials, not production credentials.

---

## 5. Test Data Management

Test data will be maintained separately from automation logic.

### 5.1 Data Categories

- Valid authentication credentials.
- Invalid authentication credentials.
- Locked-out user credentials.
- Valid customer checkout information.
- Missing mandatory checkout information.
- Product selection combinations.
- Product price combinations.

### 5.2 Data Management Principles

- Reuse valid test data where appropriate.
- Separate test data from test implementation.
- Avoid hardcoding sensitive information.
- Use controlled test data for repeatable execution.
- Reset application state between independent test scenarios when necessary.

---

## 6. Test Case Management

### 6.1 Test Case Identification

A standardized naming convention will be used.

Format:

`TC-SD-[MODULE]-[NUMBER]`

Examples:

- TC-SD-LOGIN-001
- TC-SD-INV-001
- TC-SD-CART-001
- TC-SD-CHK-001
- TC-SD-ORDER-001

### 6.2 Test Case Documentation Fields

Each test case will include:

1. Test Case ID
2. Test Case Title
3. Module
4. Test Scenario
5. Priority
6. Test Type
7. Preconditions
8. Test Steps
9. Test Data
10. Expected Result
11. Actual Result
12. Execution Status
13. Evidence Reference
14. Defect Reference

### 6.3 Test Case Prioritization

| Priority | Description |
|---|---|
| Critical | Essential business workflows; failure prevents core usage |
| High | Important functional behavior |
| Medium | Standard functionality with moderate business impact |
| Low | Minor UI or usability behavior |

---

## 7. Test Execution Strategy

### 7.1 Execution Cycles

| Execution ID | Description |
|---|---|
| TE-SD-001 | Initial Manual Functional Testing |
| TE-SD-002 | Manual Regression Testing |
| TE-SD-003 | Automated Regression Testing |

### 7.2 Execution Statuses

| Status | Meaning |
|---|---|
| Not Run | Test has not been executed |
| Pass | Actual result matches expected result |
| Fail | Actual result differs from expected result |
| Blocked | Test cannot be executed due to an external dependency or blocker |
| Not Applicable | Test is excluded from the current execution scope |

### 7.3 Test Evidence

Execution evidence will include:

- Screenshots of relevant application states.
- Defect reproduction screenshots.
- Execution logs.
- Automated test reports.
- Failure screenshots and traces where applicable.

Evidence will be stored in the repository's `evidence/` directory.

---

## 8. Defect Management

### 8.1 Defect Reporting

Any unexpected application behavior will be investigated and documented.

Each defect report should contain:

- Defect ID.
- Defect title.
- Related test case ID.
- Environment and browser.
- Preconditions.
- Steps to reproduce.
- Expected result.
- Actual result.
- Severity.
- Priority.
- Supporting evidence.
- Defect status.

### 8.2 Defect Severity

| Severity | Description |
|---|---|
| Critical | Application failure or major business workflow unavailable |
| High | Significant functionality is broken |
| Medium | Functional issue with an available workaround |
| Low | Minor visual or usability issue |

Severity represents technical or functional impact. Priority represents the urgency of addressing the issue.

### 8.3 Defect Lifecycle

The following lifecycle will be followed:

New → Open → In Progress → Fixed → Retest → Closed

If a defect persists during retesting, it will be reopened.

Defects will only be reported after reproducing the issue and comparing the actual behavior with the documented expected behavior.

---

## 9. Entry and Exit Criteria

### 9.1 Entry Criteria

Testing can begin when:

- The application is accessible.
- The testing scope has been defined.
- Relevant requirements have been documented.
- Test scenarios and test cases have been reviewed.
- Required test data is available.
- The test environment is ready.

### 9.2 Exit Criteria

A testing cycle can be considered complete when:

- All planned test cases have an execution status.
- Critical and high-priority test cases have been executed.
- All failures have been documented.
- Critical and high-severity defects have been investigated.
- Test evidence has been collected where required.
- The test execution summary has been prepared.
- Remaining risks and limitations have been documented.

Exit criteria do not imply that every test must pass. Outstanding defects and unexecuted tests must be transparently reported.

---

## 10. Risk Assessment

| Risk ID | Risk | Impact | Mitigation |
|---|---|---|---|
| RISK-001 | Public demo application becomes unavailable | High | Record execution limitations and retry later |
| RISK-002 | Application behavior changes | Medium | Revalidate expected behavior before execution |
| RISK-003 | Browser compatibility differences | Medium | Execute tests across selected browsers |
| RISK-004 | Dynamic UI behavior causes flaky automation | Medium | Use reliable locators and appropriate synchronization |
| RISK-005 | Test data or application state is inconsistent | Medium | Reset state and isolate test scenarios |
| RISK-006 | Automation failures are incorrectly classified | Medium | Investigate failures and preserve evidence |

---

## 11. Roles and Responsibilities

This is an individual portfolio project.

| Role | Responsibility |
|---|---|
| QA Engineer | Test planning, test design, manual execution, defect reporting |
| Automation Engineer | Framework design, scripting, debugging, automation maintenance |
| Test Reviewer | Review test coverage, documentation, and implementation quality |

The same project contributor may perform multiple roles.

---

## 12. Test Deliverables

The project will produce the following deliverables:

| Deliverable | Repository Location |
|---|---|
| Software Test Plan | docs/test-plan.md |
| Test Strategy | docs/test-strategy.md |
| Functional Requirements | docs/requirements/ |
| Manual Test Cases | docs/test-cases/ |
| Test Data Documentation | docs/test-data.md |
| Traceability Matrix | docs/traceability-matrix.md |
| Execution Report | docs/test-execution-report.md |
| Test Summary Report | docs/test-summary-report.md |
| Defect Reports | bug-reports/ |
| Test Evidence | evidence/ |
| Playwright Framework | automation/ |
| CI/CD Workflow | .github/workflows/ |

---

## 13. Test Metrics and Reporting

The following metrics will be used to evaluate testing progress and coverage.

### Test Execution Metrics

**Test Execution Progress**

Executed Test Cases / Total Planned Test Cases × 100

**Pass Rate**

Passed Test Cases / Executed Test Cases × 100

**Fail Rate**

Failed Test Cases / Executed Test Cases × 100

**Requirement Coverage**

Requirements Covered by Tests / Total In-Scope Requirements × 100

### Defect Metrics

- Total defects identified.
- Defects by severity.
- Open versus closed defects.
- Defect retest results.
- Defect distribution by functional module.

All metrics will be based on actual recorded execution data, not planned test counts.

---

## 14. Assumptions and Constraints

### Assumptions

- SauceDemo is available for testing.
- Public demonstration accounts remain accessible.
- The application supports the documented core shopping workflows.
- No real customer or payment data is required.
- Testing is conducted for educational and portfolio purposes.

### Constraints

- The team has no access to the application's internal source code.
- Backend implementation and database behavior cannot be directly verified.
- The public application may change without notice.
- External environment availability may affect execution.
- Test results are limited to the observable behavior of the application.

---

## 15. Approval and Document Control

| Version | Date | Description | Status |
|---|---|---|---|
| 1.0 | 2026-11-13 | Initial test plan creation | Draft |

**Document Review Checklist**

- [ ] Scope reviewed.
- [ ] Testing objectives reviewed.
- [ ] Testing approach reviewed.
- [ ] Environment requirements reviewed.
- [ ] Risks identified.
- [ ] Entry and exit criteria defined.
- [ ] Deliverables identified.

---

**End of Document**

*SauceDemo Quality Engineering Project – Software Test Plan v1.0*
