# Functional Requirements

The following functional requirements define the functional testing scope for the SauceDemo application.

## Login / Authentication

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-LOGIN-001 | User can log in with valid credentials. | High |
| FR-LOGIN-002 | Application rejects invalid login credentials. | High |
| FR-LOGIN-003 | Application validates required login fields. | High |
| FR-LOGIN-004 | Application prevents a locked or restricted user from logging in successfully. | High |

## Product Listing / Inventory

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-PRODUCT-001 | Products are displayed after successful login. | High |
| FR-PRODUCT-002 | Products display the expected name, price, and image information. | Medium |
| FR-PRODUCT-003 | User can sort products using the available sorting options. | Medium |
| FR-PRODUCT-004 | User can add a product to the cart from the Products page. | High |

## Product Details

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-DETAILS-001 | User can open a product details page from the Products page. | Medium |
| FR-DETAILS-002 | Product Details displays the information corresponding to the selected product. | Medium |
| FR-DETAILS-003 | User can add the selected product to the cart from the Product Details page. | High |

## Shopping Cart

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-CART-001 | User can add products to the cart and the selected products are displayed correctly in the shopping cart. | High |
| FR-CART-002 | User can remove a product from the shopping cart. | High |
| FR-CART-003 | User can continue shopping from the shopping cart. | Medium |
| FR-CART-004 | User can proceed from the shopping cart to checkout. | High |

## Checkout

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-CHECKOUT-001 | User can enter the required checkout information. | High |
| FR-CHECKOUT-002 | Application validates required checkout information. | High |
| FR-CHECKOUT-003 | Application displays an order overview before order completion. | High |
| FR-CHECKOUT-004 | User can cancel checkout and return to the shopping flow. | Medium |

## Order Completion

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-ORDER-001 | User can complete an order with valid checkout information. | High |
| FR-ORDER-002 | Application displays an order confirmation after successful order completion. | High |
| FR-ORDER-003 | Application returns to an appropriate shopping state after order completion. | Medium |

## Session Management

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-SESSION-001 | Authenticated user can log out. | High |
| FR-SESSION-002 | Authenticated pages cannot be accessed after logout. | High |
| FR-SESSION-003 | Supported application navigation maintains the expected authenticated session state. | Medium |

## Cross-Module Behavior

| Requirement ID | Requirement | Priority |
|---|---|---|
| FR-CROSS-001 | Product information remains consistent when moving from Products to Product Details to Cart. | High |
| FR-CROSS-002 | Selected products remain consistent when progressing from Cart through Checkout to Order Completion. | High |

## Requirement Traceability

Each functional requirement is intended to be connected to its corresponding:

**Requirement → Scenario → Test Case → Execution Result → Defect (if applicable)**

Requirement IDs remain consistent throughout the project documentation.

## Requirement Coverage

| Module | Number of Requirements |
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