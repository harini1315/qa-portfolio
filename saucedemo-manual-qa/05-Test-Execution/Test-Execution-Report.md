# Test Execution Report

## 1. Execution Overview

Manual execution was performed against the SauceDemo / Swag Labs web application using the available SauceDemo test personas.

The formal test execution covered the documented test cases across the following application areas:

- Login and Authentication
- Product Listing / Inventory
- Product Details
- Shopping Cart
- Checkout
- Order Completion
- Session Management

The execution included positive scenarios, negative scenarios, user-specific behavior, cross-module validation, and end-to-end workflow testing.

## 2. Test Environment

| Item | Details |
|---|---|
| Application | SauceDemo / Swag Labs |
| URL | https://www.saucedemo.com |
| Test Type | Manual Testing |
| Testing Approach | Black-box Functional Testing |
| Test Personas | SauceDemo-provided test users |
| Execution Status | Completed for all documented test cases |

Browser and operating system details were not recorded during execution and are therefore not claimed in this report.

## 3. Formal Test Execution

A total of **37 documented test cases** were executed across the application modules.

### Execution by Module

| Module | Test Cases | Passed | Failed | Blocked |
|---|---:|---:|---:|---:|
| Login / Authentication | 5 | 5 | 0 | 0 |
| Product Listing / Inventory | 7 | 5 | 2 | 0 |
| Product Details | 4 | 3 | 1 | 0 |
| Shopping Cart | 6 | 5 | 1 | 0 |
| Checkout | 8 | 6 | 2 | 0 |
| Order Completion | 4 | 3 | 1 | 0 |
| Session Management | 3 | 3 | 0 | 0 |
| **Total** | **37** | **30** | **7** | **0** |

## 4. Failed Test Cases

Seven documented test cases failed during execution.

| Test Case ID | Module | Test Persona | Result |
|---|---|---|---|
| TC-PRODUCT-006 | Product Listing | `problem_user` | FAIL |
| TC-PRODUCT-007 | Product Listing | `problem_user` | FAIL |
| TC-DETAILS-004 | Product Details | `problem_user` | FAIL |
| TC-CART-006 | Product Interaction | `problem_user` | FAIL |
| TC-CHECKOUT-007 | Checkout | `problem_user` | FAIL |
| TC-CHECKOUT-008 | Checkout | `error_user` | FAIL |
| TC-ORDER-004 | Order Completion | `error_user` | FAIL |

The failed test cases represent observed differences between the expected and actual application behavior.

## 5. Defect-Related Findings

The seven failed test cases resulted in seven verified defect findings.

### `problem_user`

The documented failures included:

- Incorrect or identical product images displayed across the inventory.
- Product sorting options did not reorder the product list.
- Product names opened mismatched Product Details pages.
- Add to Cart / Remove controls on the Products page behaved inconsistently for certain products.
- Checkout Last Name input affected the First Name field.

### `error_user`

The documented failures included:

- The Last Name field did not accept keyboard input during checkout.
- The Finish button did not respond on the Checkout Overview page, preventing order completion.

These findings are documented in the relevant defect records.

## 6. Successful Negative Testing

Negative test scenarios were evaluated based on whether the application correctly handled invalid or restricted input.

Examples include:

- Invalid login credentials were rejected as expected.
- Blank username validation worked as expected.
- Blank password validation worked as expected.
- Locked-out user access was correctly restricted.
- Blank checkout fields were correctly validated.

These scenarios were recorded as **PASS** because the observed application behavior matched the expected result.

Expected rejection behavior is therefore not counted as a defect.

## 7. End-to-End Execution

The primary shopping workflow was executed as:

**Login → Products → Product Details → Add to Cart → Cart → Checkout → Order Completion → Logout**

The standard end-to-end workflow was successfully completed.

### E2E Result

**PASS**

The complete workflow successfully progressed through the major application modules without an observed failure during the standard execution.

## 8. Execution Summary

| Metric | Result |
|---|---:|
| Designed Test Cases | 37 |
| Executed Test Cases | 37 |
| Passed | 30 |
| Failed | 7 |
| Blocked | 0 |
| Not Executed | 0 |
| Test Case Pass Rate | 81.1% |
| Verified Defects | 7 |
| E2E Workflows Executed | 1 |
| E2E Workflows Passed | 1 |
| E2E Workflows Failed | 0 |

### Pass Rate Calculation

**Pass Rate = Passed Test Cases / Executed Test Cases × 100**

**30 / 37 × 100 = 81.1%**

## 9. Evidence

Execution results were recorded based on actual manual testing performed against the application.

Where failures were identified, the corresponding observations were documented in the relevant test cases and defect records.

## 10. Execution Conclusion

All 37 formally documented test cases were executed.

The execution resulted in:

- **30 passed test cases**
- **7 failed test cases**
- **0 blocked test cases**
- **0 not-executed test cases**
- **7 verified defects**

The standard shopping workflow was successfully completed, while user-specific testing identified functional issues in product behavior, product interaction, checkout, and order completion.

The execution results provide broader functional coverage than the original focused execution cycle and should be used as the basis for the final test summary, defect reporting, RTM, and test metrics.
