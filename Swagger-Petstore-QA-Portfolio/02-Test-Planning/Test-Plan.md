# Test Plan

## 1. Objective

The main objective of this project is to test the functional behavior of Swagger Petstore using manual testing and API testing.

The project will also provide practical experience with Jira, Postman, Browser DevTools, and Git/GitHub.

## 2. Scope

### In Scope

- Pet creation, retrieval, update, and deletion
- Finding pets by status
- Store inventory
- Store order creation, retrieval, and deletion
- User creation and login/logout
- Positive and negative testing
- API request and response validation
- Integration testing
- End-to-End testing
- Basic Browser DevTools investigation
- Jira defect tracking

### Out of Scope

- Automation testing
- Performance/load testing
- Security testing
- Database testing
- Source-code testing
- CI/CD implementation
- Testing every available API endpoint

## 3. Testing Types

| Testing Type | Purpose |
|---|---|
| Functional Testing | Check whether the application functions work as expected |
| Positive Testing | Check valid inputs and expected successful behavior |
| Negative Testing | Check how the application handles invalid inputs |
| API Testing | Validate requests, responses, and status codes |
| Integration Testing | Check whether related operations work correctly together |
| End-to-End Testing | Check complete workflows from start to finish |
| Smoke Testing | Check the main functionality before detailed testing |
| Regression Testing | Check that existing functionality still works after changes |

## 4. Test Approach

The testing will be carried out in the following order:

1. Understand the application and requirements.
2. Create test scenarios.
3. Design 15 manual test cases.
4. Prepare test data.
5. Execute the test cases.
6. Record actual results and status.
7. Investigate unexpected results.
8. Report genuine defects in Jira.
9. Retest defects when applicable.
10. Perform API testing using Postman.
11. Perform selected integration and End-to-End tests.
12. Perform smoke and regression testing using existing test cases.
13. Calculate test metrics.
14. Prepare the final test summary.

## 5. Test Environment

| Item | Details |
|---|---|
| Application | Swagger Petstore |
| API Base URL | `https://petstore.swagger.io/v2` |
| API Testing Tool | Postman |
| Defect Tracking Tool | Jira |
| Browser Investigation | Chrome/Edge DevTools |
| Version Control | Git/GitHub |

## 6. Test Data

The following types of test data will be used:

- Valid pet details
- Invalid or incomplete pet details
- Existing pet IDs
- Non-existent pet IDs
- Valid order details
- Invalid order parameters
- Valid user details
- Valid and invalid login credentials

Actual test data will be recorded during test execution.

## 7. Entry Criteria

Testing will begin when:

- Application/API is accessible.
- Required tools are available.
- Functional requirements are identified.
- Test scenarios and test cases are prepared.

## 8. Exit Criteria

Testing will be considered complete when:

- All planned test cases are executed or marked as Blocked where applicable.
- Actual results are recorded.
- Genuine defects are documented in Jira.
- Required retesting is completed.
- Smoke and regression testing are completed.
- Integration and End-to-End workflows are tested.
- Test metrics and final results are documented.

## 9. Project Targets

| Item | Target |
|---|---:|
| Manual Test Cases | 15 |
| API Tests | 6 |
| Test Scenarios | 19 | 
| Integration Workflows | 1 |
| End-to-End Workflows | 1 |
| Smoke Tests | 6 |
| Regression Tests | 6 |
| Jira Defects | 2 | 
| Automation | None |

## 10. Defect Handling

A failed test will not automatically be treated as a defect.

The following process will be followed:

```text
Unexpected Result
       ↓
Reproduce
       ↓
Verify
       ↓
Report in Jira
       ↓
Retest
       ↓
Close / Reopen
