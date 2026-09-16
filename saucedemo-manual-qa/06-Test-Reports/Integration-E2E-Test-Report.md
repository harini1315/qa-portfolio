# Integration and End-to-End Test Report

## 1. Objective

The objective of integration and end-to-end testing is to verify that related application modules work together correctly and that the major user workflow can progress across multiple application boundaries.

The testing focused on the interaction between:

- Login and Products
- Products and Product Details
- Product Details and Shopping Cart
- Shopping Cart and Checkout
- Checkout and Order Completion
- Order Completion and Session Management

## 2. Integration Test Scope

The following module interactions were evaluated as part of the documented test execution and end-to-end workflow:

- Login → Products
- Products → Product Details
- Product Details → Cart
- Cart → Checkout
- Checkout → Order Completion
- Order Completion → Logout

The cross-module requirements are:

- **FR-CROSS-001** — Product information remains consistent between Products, Product Details, and Cart.
- **FR-CROSS-002** — Selected products remain consistent from Cart through Checkout and Order Completion.

## 3. Integration Coverage

| Integration Area | Related Test Cases / Execution | Result |
|---|---|---|
| Login → Products | TC-LOGIN-001, TC-PRODUCT-001 | Pass |
| Products → Product Details | TC-DETAILS-001, TC-DETAILS-002, TC-DETAILS-004 | Pass / Fail depending on user (Pass for standard_user; Fail for problem_user)|
| Product Details → Cart | TC-DETAILS-003, TC-CART-001 | Pass |
| Cart → Checkout | TC-CART-004, TC-CHECKOUT-001 | Pass |
| Checkout → Order Completion | TC-CHECKOUT-005, TC-ORDER-001, TC-ORDER-004 | Pass / Fail depending on user(Pass for standard_user; Fail for error_user) |
| Order Completion → Logout | E2E workflow | Pass |

User-specific failures were observed during product navigation, product interaction, checkout, and order completion testing. These failures did not prevent the standard-user end-to-end workflow from completing successfully.

## 4. Cross-Module Requirement Validation

### FR-CROSS-001 — Product Information Consistency

**Flow:**

**Products → Product Details → Cart**

The standard-user workflow successfully demonstrated movement from the Products page to Product Details and then to the shopping cart.

Product information was displayed correctly for standard_user within the executed scope, while user-specific testing with problem_user identified product-related inconsistencies.

User-specific testing with `problem_user` identified inconsistencies in product behavior, including:

- Product names opening mismatched Product Details pages.
- Incorrect or identical product images being displayed.
- Product interaction behavior being inconsistent for certain products.

These findings are documented in the relevant Product, Product Details, and Cart test cases.

### FR-CROSS-002 — Selected Product Consistency

**Flow:**

**Cart → Checkout → Order Completion**

The standard-user end-to-end workflow successfully progressed from the Cart through Checkout and Order Completion.

The selected product remained part of the shopping workflow through checkout, and the order was successfully completed.

User-specific testing with `error_user` identified an order completion failure because the Finish button did not respond on the Checkout Overview page.

## 5. End-to-End Test

### E2E Workflow

**Login → Products → Product Details → Add to Cart → Cart → Checkout → Order Completion → Logout**

### Expected Result

The user should be able to progress through the complete shopping workflow without an unexpected interruption, successfully complete the order, and log out.

### Actual Result

The complete workflow was successfully executed using the `standard_user` persona.

The user successfully:

1. Logged in.
2. Accessed the Products page.
3. Opened Product Details.
4. Added a product to the cart.
5. Viewed the cart.
6. Proceeded to Checkout.
7. Submitted the order.
8. Completed the order.
9. Logged out.

### E2E Status

**PASS**

## 6. E2E Execution Summary

| Metric | Result |
|---|---:|
| E2E Workflows Executed | 1 |
| Passed | 1 |
| Failed | 0 |
| Blocked | 0 |
| E2E Pass Rate | 100% |

## 7. Integration Findings

The standard-user integration and end-to-end workflow completed successfully.

However, user-specific testing identified functional issues at several module boundaries:

| Area | User | Finding |
|---|---|---|
| Products → Product Details | `problem_user` | Product names opened mismatched Product Details pages |
| Products → Cart | `problem_user` | Add to Cart / Remove controls behaved inconsistently on the Products page |
| Checkout | `problem_user` | Last Name input affected the First Name field |
| Checkout | `error_user` | Last Name field did not accept keyboard input |
| Checkout → Order Completion | `error_user` | Finish button did not respond |

These findings are already represented in the formal test cases and defect records.

## 8. Relationship Between Integration Testing and Defects

Integration and end-to-end testing does not require every module to be defect-free for the E2E workflow to pass.

In this project:

- The **standard-user E2E workflow passed**.
- **User-specific testing identified functional failures** in individual modules and interactions.
- The identified failures were recorded as verified defects.
- The defects did not prevent completion of the standard-user E2E workflow.

Therefore, the E2E result and the overall functional test result are reported separately.

## 9. Conclusion

The standard SauceDemo shopping workflow successfully demonstrated integration across the major application modules:

**Login → Products → Product Details → Cart → Checkout → Order Completion → Logout**

The standard-user E2E workflow passed successfully.

At the same time, user-specific testing identified functional issues affecting product navigation, product interaction controls, checkout behavior, and order completion.

The integration and E2E results therefore demonstrate that the primary workflow is functional for the standard user while additional user-specific defects remain present in the application.
