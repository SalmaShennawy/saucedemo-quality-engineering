# SauceDemo | Quality Engineering & Test Automation

![Testing](https://img.shields.io/badge/Testing-Quality%20Engineering-blue)
![Python](https://img.shields.io/badge/Python-3.x-yellow)
![Playwright](https://img.shields.io/badge/Automation-Playwright-green)
![Status](https://img.shields.io/badge/Project-In%20Progress-orange)

## Project Overview

This repository contains a comprehensive Quality Engineering project focused on testing the [SauceDemo](https://www.saucedemo.com/) e-commerce web application.

The project demonstrates a structured software testing lifecycle, starting with requirements analysis and manual test design, progressing to automated UI testing using Playwright and Python, and extending to test reporting and Continuous Integration/Continuous Deployment (CI/CD).

The objective is to demonstrate practical QA engineering skills, including test planning, test case design, functional testing, automation framework development, defect management, and quality reporting.

## Project Objectives

- Develop a structured and maintainable test documentation approach.
- Design comprehensive manual test cases covering functional and negative scenarios.
- Identify potential application defects and document them systematically.
- Build a scalable UI automation framework using Playwright and Python.
- Apply the Page Object Model (POM) design pattern.
- Implement data-driven and parameterized testing.
- Generate detailed and actionable test execution reports.
- Integrate automated tests into a CI/CD pipeline using GitHub Actions.

## Application Under Test

| Attribute | Details |
|---|---|
| Application | SauceDemo |
| Application URL | https://www.saucedemo.com/ |
| Application Type | E-commerce Web Application |
| Testing Approach | Manual & Automated |
| Automation Framework | Playwright |
| Programming Language | Python |
| Test Framework | Pytest |
| Version Control | Git & GitHub |

## Testing Scope

### 1. Authentication

- Valid user login.
- Invalid username and password.
- Empty username and password.
- Locked-out user authentication.
- Login error messages.
- Logout functionality.

### 2. Product Catalog

- Product listing validation.
- Product details verification.
- Product sorting (price and name).
- Product images and descriptions.
- Product availability.

### 3. Shopping Cart

- Add products to cart.
- Remove products from cart.
- Cart item quantity validation.
- Cart badge updates.
- Cart persistence during navigation.

### 4. Checkout Process

- Checkout navigation.
- Customer information validation.
- Required field validation.
- Order summary verification.
- Price and tax calculations.
- Order completion.
- Confirmation message validation.

### 5. Navigation & UI

- Navigation menu functionality.
- Application responsiveness.
- Broken links and images.
- Button functionality.
- UI consistency.

## Test Automation Strategy

The automation framework will follow established software testing and automation engineering practices.

**Framework design:**
- Page Object Model (POM).
- Pytest fixtures.
- Data-driven testing.
- Reusable test utilities.
- Explicit assertions.
- Cross-browser testing.
- Screenshot capture on test failures.
- Automated test reporting.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Playwright | Browser automation |
| Pytest | Test execution and management |
| Git | Version control |
| GitHub | Source code and documentation |
| GitHub Actions | CI/CD automation |
| Allure Reports | Test execution reporting |

## Project Structure

```text
saucedemo-quality-engineering/
│
├── docs/
│   ├── test-plan.md
│   ├── test-strategy.md
│   ├── test-cases/
│   └── bug-reports/
│
├── tests/
│   ├── ui/
│   ├── api/
│   └── conftest.py
│
├── pages/
│   ├── login_page.py
│   ├── inventory_page.py
│   ├── cart_page.py
│   └── checkout_page.py
│
├── test_data/
│   └── test_users.json
│
├── utilities/
│
├── reports/
│
├── .github/
│   └── workflows/
│       └── playwright.yml
│
├── requirements.txt
├── pytest.ini
├── .gitignore
└── README.md
```

*Note: This represents the planned project structure and will evolve as implementation progresses.*

## Test Documentation

Test documentation will include:

- Test Plan.
- Test Strategy.
- Functional Test Scenarios.
- Detailed Manual Test Cases.
- Test Execution Results.
- Defect Reports.
- Requirements Traceability Matrix (RTM).
- Automation Coverage Report.

## Execution & Reporting

The automation suite will be designed to support:

- Local test execution.
- Headless and headed browser execution.
- Cross-browser execution.
- HTML test reports.
- Allure test reports.
- Screenshots and debugging evidence.

## CI/CD Integration

GitHub Actions will be used to automate test execution.

The planned pipeline will:
1. Trigger on code pushes and pull requests.
2. Set up the Python environment.
3. Install project dependencies.
4. Install Playwright browsers.
5. Execute the automated test suite.
6. Publish test reports and execution artifacts.

## Project Roadmap

- [ ] Repository setup and documentation.
- [ ] Application analysis and requirements review.
- [ ] Test Plan and Test Strategy.
- [ ] Manual test case design.
- [ ] Test execution and defect documentation.
- [ ] Playwright framework implementation.
- [ ] Page Object Model implementation.
- [ ] Data-driven automation.
- [ ] Negative and boundary testing.
- [ ] Test reporting and screenshots.
- [ ] GitHub Actions CI/CD integration.
- [ ] Final test execution and coverage analysis.

## Author

**Salma Shennawy**

Software Testing & Quality Engineering

Interested in Software Quality, Test Automation, Python, Playwright, and AI-driven Quality Engineering.

[GitHub Profile](https://github.com/SalmaShennawy)

---

*This is an evolving portfolio project. Documentation, implementation, and test coverage will be updated throughout the development lifecycle.*
