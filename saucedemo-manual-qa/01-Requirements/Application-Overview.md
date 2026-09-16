# Application Overview

## Project Title

SauceDemo Manual QA Testing Project

## Application

**Application:** SauceDemo / Swag Labs  
**URL:** https://www.saucedemo.com  
**Type:** Web-based e-commerce application

## Project Objective

This project demonstrates a structured Manual QA testing approach for the SauceDemo web application from a QA tester's perspective.

The project covers the software testing lifecycle from requirements analysis and test design through manual execution, defect identification, traceability, reporting, and quality assessment.

Testing includes positive scenarios, negative scenarios, user-specific behavior, cross-module validation, and end-to-end workflow testing.

## Testing Scope

The following functional areas are covered:

- Login / Authentication
- Product Listing / Inventory
- Product Details
- Shopping Cart
- Checkout
- Order Completion
- Session Management
- Cross-Module Behavior
- Integration / End-to-End Workflows

Testing also includes behavior verification using different SauceDemo test users, including `standard_user`, `locked_out_user`, `problem_user`, and `error_user`.

## Testing Types

The project includes the following testing types:

- Functional Testing
- Positive Testing
- Negative Testing
- Smoke Testing
- Regression Testing
- Integration Testing
- End-to-End Testing

## QA Activities

The following QA activities are demonstrated:

- Requirements analysis
- Test scenario design
- Test case design
- Test data preparation
- Manual test execution
- Defect identification and reporting
- Requirements Traceability Matrix (RTM)
- Test execution metrics
- Smoke testing
- Regression testing
- Integration and End-to-End testing
- Test summary reporting

## Test Execution Approach

Testing was performed manually using black-box testing techniques.

Test cases were designed from the documented functional requirements and executed against the SauceDemo application.

The execution included:

- Positive functional scenarios
- Negative validation scenarios
- Standard-user workflow validation
- User-specific behavior testing
- Cross-module behavior
- End-to-end workflow validation

A total of **37 test cases were executed** during the final test execution.

## Test Results Overview

The final execution produced the following results:

| Metric | Result |
|---|---:|
| Functional Requirements | 27 |
| Requirements with Test Coverage | 27 |
| Designed Test Cases | 37 |
| Test Cases Executed | 37 |
| Test Cases Passed | 30 |
| Test Cases Failed | 7 |
| Test Cases Blocked | 0 |
| Test Cases Not Executed | 0 |
| Verified Defects | 7 |

The identified failures were primarily associated with user-specific behavior observed with `problem_user` and `error_user`.

## User-Specific Testing

The project uses SauceDemo-provided test personas to verify different application behaviors.

### `standard_user`

Used for primary functional testing and validation of the normal shopping workflow.

### `locked_out_user`

Used to verify that restricted users cannot successfully log in.

### `problem_user`

Used to identify application-specific functional issues affecting areas such as:

- Product images
- Product sorting
- Product-to-details navigation
- Product-page Add to Cart / Remove controls
- Checkout form behavior

### `error_user`

Used to identify application-specific issues affecting areas such as:

- Checkout form input
- Order completion

Only behavior that was actually observed during testing is documented as a result or defect.

## Cross-Module and End-to-End Testing

The project verifies interactions between major application modules, including:

- Products → Product Details
- Product Details → Cart
- Cart → Checkout
- Checkout → Order Completion

The primary end-to-end workflow was executed as:

**Login → Products → Product Details → Add to Cart → Cart → Checkout → Order Completion → Logout**

The standard-user end-to-end workflow completed successfully.

User-specific testing was also performed separately to identify defects in individual application areas.

## Defect Identification

The final execution identified **7 verified defects**.

These defects were identified from observed mismatches between expected and actual application behavior.

Negative scenarios such as invalid credentials, blank required fields, and locked-user access were recorded as **PASS** when the application correctly rejected the invalid input or restricted access.

## Out of Scope

The following testing activities are outside the scope of this project:

- Automation testing
- API testing
- Performance testing
- Security testing
- Database testing
- Mobile application testing

## Project Approach

The project focuses on meaningful functional coverage rather than creating a large volume of repetitive test documentation.

Test cases, execution results, defects, metrics, and reports are based on actual testing performed against the application.

The documentation is structured to demonstrate traceability from requirements through test scenarios, test cases, execution results, and defects.

## Expected Outcome

The completed repository demonstrates practical entry-level Manual QA skills and provides a structured, recruiter-friendly example of the software testing lifecycle.

The project demonstrates the ability to:

- Analyze functional requirements
- Design meaningful test scenarios and test cases
- Execute positive and negative tests
- Validate cross-module and end-to-end workflows
- Identify and document application defects
- Maintain requirements traceability
- Analyze test execution results
- Prepare professional QA reports
