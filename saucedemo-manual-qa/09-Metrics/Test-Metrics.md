# Test Metrics

## 1. Execution Metrics

| Metric | Result |
|---|---:|
| Total Functional Requirements | 27 |
| Requirements Covered by Test Cases | 27 |
| Requirement Coverage | 100% |
| Total Designed Test Cases | 37 |
| Test Cases Executed | 37 |
| Test Cases Passed | 30 |
| Test Cases Failed | 7 |
| Test Cases Blocked | 0 |
| Test Cases Not Executed | 0 |
| Test Case Execution Coverage | 100% |
| Test Case Pass Percentage | 81.1% |
| Verified Defects | 7 |

## 2. Requirement Coverage

All 27 functional requirements have at least one associated test scenario and test case.

**Requirement Coverage: 100%**

This represents the percentage of documented requirements that have corresponding test coverage.

Requirement coverage should not be interpreted as a 100% defect-free result.

## 3. Test Execution Coverage

All 37 designed test cases were executed during the final test cycle.

**Execution Coverage: 100%**

Calculation:

**37 Executed / 37 Designed × 100 = 100%**

No designed test cases remain in the **Not Executed** state.

## 4. Test Result Distribution

| Status | Count | Percentage of Executed Tests |
|---|---:|---:|
| Passed | 30 | 81.1% |
| Failed | 7 | 18.9% |
| Blocked | 0 | 0% |
| Total Executed | 37 | 100% |

### Pass Percentage

**30 / 37 × 100 = 81.1%**

### Fail Percentage

**7 / 37 × 100 = 18.9%**

## 5. Defect Metrics

| Metric | Result |
|---|---:|
| Verified Defects | 7 |
| Critical Severity Defects | 0 |
| High Severity Defects | 0 |
| Medium Severity Defects | 7 |
| Low Severity Defects | 0 |

The seven verified defects were identified from the seven failed test cases.

## 6. Defect Distribution by Module

| Module / Area | Verified Defects |
|---|---:|
| Product Inventory | 2 |
| Product Details | 1 |
| Product Interaction | 1 |
| Checkout | 2 |
| Order Completion | 1 |
| **Total** | **7** |

## 7. E2E Metrics

| Metric | Result |
|---|---:|
| E2E Workflows Executed | 1 |
| E2E Workflows Passed | 1 |
| E2E Workflows Failed | 0 |
| E2E Workflows Blocked | 0 |
| E2E Test Pass Rate| 100% |

The standard-user end-to-end workflow was successfully completed:

**Login → Products → Product Details → Add to Cart → Cart → Checkout → Order Completion → Logout**

## 8. Smoke Test Metrics

| Metric | Result |
|---|---:|
| Smoke Tests Executed | 7 |
| Smoke Tests Passed | 7 |
| Smoke Tests Failed | 0 |
| Smoke Tests Blocked | 0 |
| Smoke Test Pass Rate | 100% |

The smoke result represents only the selected critical smoke suite and should not be interpreted as the result of the complete 37-test-case suite.

## 9. Regression Test Metrics

| Metric | Result |
|---|---:|
| Regression Tests Selected | 20 |
| Regression Tests Executed | 20 |
| Regression Tests Passed | 13 |
| Regression Tests Failed | 7 |
| Regression Tests Blocked | 0 |
| Regression Tests Not Executed | 0 |
| Regression Test Pass Rate | 65.0% |


The regression result represents the selected regression suite executed during the project.

## 10. Metrics Interpretation

The final functional test execution achieved:

- **100% requirement coverage**
- **100% test execution coverage**
- **81.1% overall test case pass rate**
- **18.9% test case failure rate**
- **7 verified defects**
- **100% smoke test pass rate**
- **65.0% selected regression test pass rate**
- **100% standard-user E2E workflow pass rate**

The 100% smoke and E2E results apply only to their respective selected execution scopes. The selected regression suite achieved a 65.0% pass rate, with 13 tests passed and 7 tests failed.

The overall test result is **30 passed and 7 failed out of 37 executed test cases**.

The identified failures were primarily associated with user-specific application behavior observed during testing with `problem_user` and `error_user`.

## 11. Final Quality Indicator

Based on the completed test execution, the application successfully supported the primary standard-user shopping workflow.

However, the seven verified defects identified during broader functional and user-specific testing mean that the application should **not be considered defect-free** based on the executed scope.

The failed scenarios should be investigated, fixed, and subsequently re-tested as part of a future regression cycle.

