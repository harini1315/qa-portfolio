# Test Scenarios

The following test scenarios are derived from the functional requirements defined in `01-Requirements/Functional-Requirements.md`.

The scenarios cover positive, negative, standard-user, and user-specific behavior identified during manual testing.

## Login / Authentication

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-LOGIN-001 | FR-LOGIN-001 | Login | Verify successful login with valid credentials. | High |
| TS-LOGIN-002 | FR-LOGIN-002 | Login | Verify login behavior with invalid credentials. | High |
| TS-LOGIN-003 | FR-LOGIN-003 | Login | Verify validation of required login fields. | High |
| TS-LOGIN-004 | FR-LOGIN-004 | Login | Verify login restriction for a locked or restricted user. | High |

## Product Listing / Inventory

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-PRODUCT-001 | FR-PRODUCT-001 | Products | Verify products are displayed after successful login. | High |
| TS-PRODUCT-002 | FR-PRODUCT-002 | Products | Verify product names, prices, and images are displayed correctly. | Medium |
| TS-PRODUCT-003 | FR-PRODUCT-003 | Products | Verify product sorting using the available sorting options. | Medium |
| TS-PRODUCT-004 | FR-PRODUCT-004 | Products | Verify a product can be added to the cart from the Products page. | High |

## Product Details

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-DETAILS-001 | FR-DETAILS-001 | Product Details | Verify a product details page can be opened from the Products page. | Medium |
| TS-DETAILS-002 | FR-DETAILS-002 | Product Details | Verify the Product Details page displays information corresponding to the selected product. | Medium |
| TS-DETAILS-003 | FR-DETAILS-003 | Product Details | Verify a selected product can be added to the cart from the Product Details page. | High |

## Shopping Cart

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-CART-001 | FR-CART-001 | Cart | Verify products added to the cart are displayed correctly in the shopping cart. | High |
| TS-CART-002 | FR-CART-002 | Cart | Verify a product can be removed from the shopping cart. | High |
| TS-CART-003 | FR-CART-003 | Cart | Verify the user can continue shopping from the shopping cart. | Medium |
| TS-CART-004 | FR-CART-004 | Cart | Verify the user can proceed from the shopping cart to checkout. | High |

## Checkout

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-CHECKOUT-001 | FR-CHECKOUT-001 | Checkout | Verify required checkout information can be entered and submitted. | High |
| TS-CHECKOUT-002 | FR-CHECKOUT-002 | Checkout | Verify validation when required checkout information is missing. | High |
| TS-CHECKOUT-003 | FR-CHECKOUT-003 | Checkout | Verify the order overview displays the selected product and order information before completion. | High |
| TS-CHECKOUT-004 | FR-CHECKOUT-004 | Checkout | Verify checkout can be cancelled and the user can return to the shopping flow. | Medium |

## Order Completion

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-ORDER-001 | FR-ORDER-001 | Order | Verify an order can be completed using valid checkout information. | High |
| TS-ORDER-002 | FR-ORDER-002 | Order | Verify order confirmation is displayed after successful order completion. | High |
| TS-ORDER-003 | FR-ORDER-003 | Order | Verify the application returns to an appropriate shopping state after order completion. | Medium |

## Session Management

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-SESSION-001 | FR-SESSION-001 | Session | Verify an authenticated user can log out. | High |
| TS-SESSION-002 | FR-SESSION-002 | Session | Verify authenticated pages cannot be accessed after logout. | High |
| TS-SESSION-003 | FR-SESSION-003 | Session | Verify supported application navigation maintains the expected authenticated session state. | Medium |

## Cross-Module Behavior

| Scenario ID | Requirement ID | Module | Scenario | Priority |
|---|---|---|---|---|
| TS-CROSS-001 | FR-CROSS-001 | Cross-Module | Verify product information remains consistent when moving from Products to Product Details to Cart. | High |
| TS-CROSS-002 | FR-CROSS-002 | Cross-Module | Verify selected products remain consistent when progressing from Cart through Checkout to Order Completion. | High |

## Scenario Coverage Summary

| Module | Scenarios |
|---|---:|
| Login / Authentication | 4 |
| Product Listing / Inventory | 4 |
| Product Details | 3 |
| Shopping Cart | 4 |
| Checkout | 4 |
| Order Completion | 3 |
| Session Management | 3 |
| Cross-Module Behavior | 2 |
| **Total** | **27** |