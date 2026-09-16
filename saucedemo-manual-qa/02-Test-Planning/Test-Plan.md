# Test Plan

## 1. Objective

The objective of this test plan is to define the approach for manually testing the SauceDemo web application and verifying the functional requirements within the project scope.

The testing approach includes positive and negative functional testing, user-specific behavior testing, cross-module validation, integration testing, and end-to-end workflow testing.

## 2. Application Under Test

**Application:** SauceDemo / Swag Labs  
**URL:** https://www.saucedemo.com  
**Application Type:** Web-based e-commerce application

## 3. Scope

Testing covers:

- Login and authentication
- Product listing and inventory
- Product details
- Shopping cart
- Checkout
- Order completion
- Session management
- Cross-module behavior
- Integration and end-to-end workflows
- Negative scenarios
- User-specific application behavior

The final execution includes testing with multiple SauceDemo-provided test users, including:

- `standard_user`
- `locked_out_user`
- `problem_user`
- `error_user`

## 4. Testing Types

The following testing types are included in the project:

- Functional Testing
- Positive Testing
- Negative Testing
- Smoke Testing
- Regression Testing
- Integration Testing
- End-to-End Testing

## 5. Test Approach

Testing is performed manually using black-box testing techniques.

Test cases are designed from the documented functional requirements and include meaningful positive, negative, and user-specific scenarios.

Testing covers both normal application behavior and intentionally observable behavior associated with SauceDemo test personas.

Priority is given to critical user journeys such as:

**Login → Products → Product Details → Cart → Checkout → Order Completion → Logout**

The final test execution includes all documented test cases.

Execution results are recorded based on actual observed application behavior.

## 6. Test Environment

The following environment details apply to the test execution:

- Operating System: Not recorded
- Browser: Not recorded
- Browser Version: Not recorded
- Application URL: https://www.saucedemo.com

Environment details that were not captured during execution are not assumed or fabricated.

## 7. Test Data

SauceDemo-provided test users and valid checkout information are used during testing.

Test data is documented separately in:

`04-Test-Data/Test-Data.md`

The primary test users used during execution include:

- `standard_user` for normal functional workflow validation
- `locked_out_user` for login restriction testing
- `problem_user` for user-specific behavior testing
- `error_user` for user-specific behavior testing

## 8. Entry Criteria

Testing can begin when:

- The application is accessible.
- Functional requirements have been identified.
- Test scenarios and test cases are prepared.
- Required test data is available.
- The test environment is suitable for manual execution.

## 9. Exit Criteria

Testing is considered complete when:

- Planned test cases have been executed.
- Execution results have been recorded.
- Identified defects have been documented.
- RTM coverage has been reviewed.
- Smoke, regression, integration, and E2E results have been documented.
- Test metrics have been calculated.
- Final test results have been reviewed.

## 10. Deliverables

The project produces:

- Functional Requirements
- Test Plan
- Test Scenarios
- Test Cases
- Test Data
- Test Execution Report
- Defect Reports
- Requirements Traceability Matrix (RTM)
- Smoke Test Report
- Regression Test Report
- Integration/E2E Test Report
- Test Metrics
- Final Test Summary
- README

## 11. Risks and Limitations

- SauceDemo is a publicly available demonstration application and may change over time.
- Application behavior may vary depending on the test user or application state.
- User-specific behavior may intentionally differ between SauceDemo test personas.
- Browser and operating system details were not recorded during execution.
- Only behavior that was actually observed during testing is reported as a test result or defect.
- A failed test case represents an observed mismatch between expected and actual behavior; defect reporting is based on verified application behavior.

## 12. Test Status Definitions

| Status | Meaning |
|---|---|
| Not Executed | Test has been designed but has not been performed. |
| Pass | Actual behavior matches the expected result. |
| Fail | Actual behavior does not match the expected result. |
| Blocked | Test cannot be completed because of an external blocker or dependency. |
