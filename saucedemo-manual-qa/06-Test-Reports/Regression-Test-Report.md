# Regression Test Report

## 1. Objective

The objective of regression testing is to verify that previously validated application functionality continues to behave as expected across the application's major functional areas.

For this portfolio project, regression testing was performed using a selected set of functional test cases from the documented test suite.

The regression scope included standard user workflows, negative scenarios, and selected user-specific scenarios.

## 2. Regression Scope

The regression scope covered the following areas:

- Login and Authentication
- Product Listing / Inventory
- Product Details
- Shopping Cart
- Checkout
- Order Completion
- Session Management
- User-Specific Functional Behavior

The regression suite consisted of 20 selected test cases from the 37-test-case functional test suite. The selected cases covered standard-user workflows, negative scenarios, and selected test-persona-specific scenarios.

## 3. Selected Regression Tests

| Test Case ID | Module | Purpose | User | Result |
|---|---|---|---|---|
| TC-LOGIN-001 | Login | Verify valid login | `standard_user` | PASS |
| TC-LOGIN-002 | Login | Verify invalid credentials are rejected | `standard_user` | PASS |
| TC-LOGIN-005 | Login | Verify locked-out user behavior | `locked_out_user` | PASS |
| TC-PRODUCT-001 | Products | Verify products are displayed | `standard_user` | PASS |
| TC-PRODUCT-003 | Products | Verify product sorting | `standard_user` | PASS |
| TC-PRODUCT-005 | Products | Verify product can be added to cart | `standard_user` | PASS |
| TC-PRODUCT-006 | Products | Verify product images | `problem_user` | FAIL |
| TC-PRODUCT-007 | Products | Verify product sorting | `problem_user` | FAIL |
| TC-DETAILS-002 | Product Details | Verify product information | `standard_user` | PASS |
| TC-DETAILS-004 | Product Details | Verify product-to-details navigation | `problem_user` | FAIL |
| TC-CART-002 | Cart | Verify product removal | `standard_user` | PASS |
| TC-CART-006 | Product Interaction | Verify Add to Cart / Remove behavior | `problem_user` | FAIL |
| TC-CHECKOUT-001 | Checkout | Verify valid checkout information | `standard_user` | PASS |
| TC-CHECKOUT-002 | Checkout | Verify required-field validation | `standard_user` | PASS |
| TC-CHECKOUT-005 | Checkout | Verify order overview | `standard_user` | PASS |
| TC-CHECKOUT-007 | Checkout | Verify checkout field behavior | `problem_user` | FAIL |
| TC-CHECKOUT-008 | Checkout | Verify checkout form behavior | `error_user` | FAIL |
| TC-ORDER-001 | Order Completion | Verify order completion | `standard_user` | PASS |
| TC-ORDER-004 | Order Completion | Verify order completion | `error_user` | FAIL |
| TC-SESSION-001 | Session Management | Verify logout | `standard_user` | PASS |

## 4. Regression Result

| Metric | Result |
|---|---:|
| Selected Regression Tests | 20 |
| Executed | 20 |
| Passed | 13 |
| Failed | 7 |
| Blocked | 0 |
| Not Executed | 0 |
| Regression Test Pass Rate | 65.0% |
| Verified Defects | 7 |

### Pass Rate Calculation

**Pass Rate = Passed Tests / Executed Tests × 100**

**13 / 20 × 100 = 65.0%**

## 5. Regression Findings

The selected regression suite confirmed that the standard application workflow continued to function correctly for the tested standard-user scenarios.

However, user-specific regression testing identified failures associated with `problem_user` and `error_user`.

The identified issues included:

- Incorrect product images for `problem_user`.
- Product sorting failure for `problem_user`.
- Mismatched Product Details navigation for `problem_user`.
- Inconsistent Add to Cart / Remove controls on the Products page for `problem_user`.
- Checkout field interaction issue for `problem_user`.
- Last Name field input failure for `error_user`.
- Finish button failure for `error_user`.

These failures correspond to the seven verified defects identified during the overall test execution.

## 6. Standard User Regression Result

The selected standard-user regression scenarios passed successfully across the major shopping workflow.

The following areas were successfully validated:

- Login
- Product listing
- Product sorting
- Add to Cart
- Product Details
- Shopping Cart
- Checkout
- Order Completion
- Logout

The standard-user E2E workflow also completed successfully.

## 7. User-Specific Regression Result

User-specific regression testing demonstrated that application behavior was not consistent across all test personas.

### `problem_user`

Failures were identified in:

- Product images
- Product sorting
- Product-to-details navigation
- Products-page Add to Cart / Remove controls
- Checkout field behavior

### `error_user`

Failures were identified in:

- Checkout Last Name field
- Order completion through the Finish button

## 8. Relationship Between Regression and Defects

A failed regression test indicates that the observed application behavior did not meet the expected result.

In this project, the seven failed regression scenarios correspond to seven verified defects.

The defects are documented separately and should be re-tested after corrective changes are implemented.

## 9. Regression Recommendation

The identified failed regression scenarios should be re-executed after the corresponding defects are fixed.

Regression testing should confirm that:

- Previously failing functionality now behaves as expected.
- Fixes do not introduce new failures in related modules.
- The standard-user shopping workflow continues to work.
- User-specific application behavior is revalidated.

## 10. Conclusion

The selected regression suite successfully validated the core standard-user functionality but identified several user-specific failures.

The regression execution resulted in:

- **20 selected regression tests**
- **20 executed**
- **13 passed**
- **7 failed**
- **0 blocked**
- **7 verified defects**

The results demonstrate the importance of including different application personas in regression testing rather than validating only the standard-user workflow.
