# Requirements Traceability Matrix (RTM)

## 1. Purpose

This Requirements Traceability Matrix (RTM) maps each functional requirement to its related test scenario and test case.

The RTM also records the final execution result and associated defect ID where a verified defect was identified.

The traceability flow used in this project is:

**Requirement → Scenario → Test Case → Execution Result → Defect (if applicable)**

## 2. Traceability Matrix

| Requirement ID | Requirement | Priority | Scenario ID | Test Case ID(s) | Execution Status | Defect ID |
|---|---|---|---|---|---|---|
| FR-LOGIN-001 | User can log in with valid credentials. | High | TS-LOGIN-001 | TC-LOGIN-001 | Pass | — |
| FR-LOGIN-002 | Application rejects invalid login credentials. | High | TS-LOGIN-002 | TC-LOGIN-002 | Pass | — |
| FR-LOGIN-003 | Application validates required login fields. | High | TS-LOGIN-003 | TC-LOGIN-003, TC-LOGIN-004 | Pass | — |
| FR-LOGIN-004 | Application handles a locked/restricted user appropriately. | High | TS-LOGIN-004 | TC-LOGIN-005 | Pass | — |
| FR-PRODUCT-001 | Products are displayed after successful login. | High | TS-PRODUCT-001 | TC-PRODUCT-001 | Pass | — |
| FR-PRODUCT-002 | Products display their name, price, and image. | Medium | TS-PRODUCT-002 | TC-PRODUCT-002, TC-PRODUCT-006 | Fail | BUG-001 |
| FR-PRODUCT-003 | User can sort products using available sorting options. | Medium | TS-PRODUCT-003 | TC-PRODUCT-003, TC-PRODUCT-004, TC-PRODUCT-007 | Fail | BUG-002 |
| FR-PRODUCT-004 | User can add a product to the cart from the Products page. | High | TS-PRODUCT-004 | TC-PRODUCT-005 | Pass | — |
| FR-DETAILS-001 | User can open a product details page. | Medium | TS-DETAILS-001 | TC-DETAILS-001, TC-DETAILS-004 | Fail | BUG-003 |
| FR-DETAILS-002 | Product details display the selected product information. | Medium | TS-DETAILS-002 | TC-DETAILS-002 | Pass | — |
| FR-DETAILS-003 | A product added from its details page is added as the selected product. | High | TS-DETAILS-003 | TC-DETAILS-003 | Pass | — |
| FR-CART-001 | Added products are displayed in the shopping cart. | High | TS-CART-001 | TC-CART-001, TC-CART-005 | Pass | — |
| FR-CART-002 | User can remove a product from the cart. | High | TS-CART-002 | TC-CART-002 | Pass | — |
| FR-CART-003 | User can continue shopping from the cart. | Medium | TS-CART-003 | TC-CART-003 | Pass | — |
| FR-CART-004 | User can proceed from the cart to checkout. | High | TS-CART-004 | TC-CART-004 | Pass | — |
| FR-CART-005 | User can add and remove products using the cart controls from the Products page. | High | TS-CART-005 | TC-CART-006 | Fail | BUG-004 |
| FR-CHECKOUT-001 | User can enter the required checkout information. | High | TS-CHECKOUT-001 | TC-CHECKOUT-001, TC-CHECKOUT-007, TC-CHECKOUT-008 | Fail | BUG-005, BUG-006 |
| FR-CHECKOUT-002 | Application validates required checkout information. | High | TS-CHECKOUT-002 | TC-CHECKOUT-002, TC-CHECKOUT-003, TC-CHECKOUT-004 | Pass | — |
| FR-CHECKOUT-003 | Application displays an order overview before completion. | High | TS-CHECKOUT-003 | TC-CHECKOUT-005 | Pass | — |
| FR-CHECKOUT-004 | User can cancel checkout and return to the shopping flow. | Medium | TS-CHECKOUT-004 | TC-CHECKOUT-006 | Pass | — |
| FR-ORDER-001 | User can complete an order with valid checkout information. | High | TS-ORDER-001 | TC-ORDER-001, TC-ORDER-004 | Fail | BUG-007 |
| FR-ORDER-002 | Application displays an order confirmation after successful completion. | High | TS-ORDER-002 | TC-ORDER-002 | Pass | — |
| FR-ORDER-003 | Application updates the shopping state appropriately after order completion. | Medium | TS-ORDER-003 | TC-ORDER-003 | Pass | — |
| FR-SESSION-001 | Authenticated user can log out. | High | TS-SESSION-001 | TC-SESSION-001 | Pass | — |
| FR-SESSION-002 | User is returned to the unauthenticated state after logout. | High | TS-SESSION-002 | TC-SESSION-002 | Pass | — |
| FR-SESSION-003 | Supported navigation maintains the expected session state. | Medium | TS-SESSION-003 | TC-SESSION-003 | Pass | — |

## 3. Cross-Module Traceability

Cross-module behavior was validated through the related functional test cases and the end-to-end workflow.

### FR-CROSS-001

**Requirement:** Product information remains consistent between Products, Product Details, and Cart.

**Related areas:**

**Products → Product Details → Cart**

Relevant test cases include:

- TC-PRODUCT-002
- TC-DETAILS-002
- TC-DETAILS-003
- TC-CART-001
- TC-CART-005

The end-to-end workflow also passed through these application modules using the standard user.

The product-specific failures identified with `problem_user` are documented separately under the affected product and interaction requirements.

### FR-CROSS-002

**Requirement:** Selected products remain consistent from Cart through Checkout and Order Completion.

**Related areas:**

**Cart → Checkout → Order Completion**

Relevant test cases include:

- TC-CART-001
- TC-CART-005
- TC-CHECKOUT-005
- TC-ORDER-001
- TC-ORDER-002
- TC-ORDER-003

The complete standard-user E2E workflow successfully progressed through Cart, Checkout, and Order Completion.

## 4. Coverage Summary

| Metric | Result |
|---|---:|
| Total Functional Requirements | 27 |
| Requirements with Test Coverage | 27 |
| Requirements without Test Coverage | 0 |
| Requirement Coverage | 100% |
| Total Designed Test Cases | 37 |
| Test Cases Executed | 37 |
| Test Cases Passed | 30 |
| Test Cases Failed | 7 |
| Test Cases Blocked | 0 |
| Test Cases Not Executed | 0 |
| Verified Defects | 7 |



## 5. Requirement Result Summary

| Result | Requirements |
|---|---:|
| Requirements with all related tests passing | 20 |
| Requirements with at least one failed related test | 7 |
| Total Requirements | 27 |

A requirement is considered affected when at least one associated test case failed.

The presence of a failed test case does not mean every test case associated with that requirement failed.

## 6. Defect Traceability

The seven verified defects identified during execution are linked to their corresponding failed test cases and requirements.

| Defect ID | Related Test Case | Requirement ID | Module |
|---|---|---|---|
| BUG-001 | TC-PRODUCT-006 | FR-PRODUCT-002 | Product Inventory |
| BUG-002 | TC-PRODUCT-007 | FR-PRODUCT-003 | Product Inventory |
| BUG-003 | TC-DETAILS-004 | FR-DETAILS-001 | Product Details |
| BUG-004 | TC-CART-006 | FR-CART-005 | Product Interaction |
| BUG-005 | TC-CHECKOUT-007 | FR-CHECKOUT-001 | Checkout |
| BUG-006 | TC-CHECKOUT-008 | FR-CHECKOUT-001 | Checkout |
| BUG-007 | TC-ORDER-004 | FR-ORDER-001 | Order Completion |

## 7. Traceability Status

All functional requirements defined for this project have associated test scenarios and test cases.

All 37 designed test cases were executed.

The final execution result was:

**37 Executed → 30 Passed → 7 Failed → 7 Verified Defects**

The RTM therefore provides traceability from the documented requirements through test execution and, where applicable, defect identification.

## 8. Important Note

The RTM records results based on the actual test cases executed during the project.

Expected negative behavior, such as invalid login rejection, required-field validation, and locked-user restriction, is recorded as **Pass** when the application behaves as expected.

The seven failed test cases represent observed behavior that did not match the corresponding expected results and were therefore linked to verified defects.

