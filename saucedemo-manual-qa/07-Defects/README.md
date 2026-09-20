# Defects

## 1. Defect Summary

A total of **7 verified defects** were identified during manual execution of the SauceDemo test suite.

The defects were identified while testing different application users, including `problem_user` and `error_user`.

| Metric | Result |
|---|---:|
| Verified Defects | 7 |
| Related Failed Test Cases | 7 |
| Critical Severity Defects | 0 |
| High Severity Defects | 0 |
| Medium Severity Defects | 7 |
| Low Severity Defects | 0 |

## 2. Identified Defects

| Defect ID | Module | User | Related Test Case | Summary |
|---|---|---|---|---|
| BUG-001 | Product Inventory | `problem_user` | TC-PRODUCT-006 | Incorrect/identical product images are displayed. |
| BUG-002 | Product Inventory | `problem_user` | TC-PRODUCT-007 | Product sorting options do not reorder the product list. |
| BUG-003 | Product Details | `problem_user` | TC-DETAILS-004 | Product names open mismatched Product Details pages. |
| BUG-004 | Product Interaction | `problem_user` | TC-CART-006 | Add to Cart / Remove behavior is inconsistent on the Products page. |
| BUG-005 | Checkout | `problem_user` | TC-CHECKOUT-007 | Last Name input also affects the First Name field. |
| BUG-006 | Checkout | `error_user` | TC-CHECKOUT-008 | Last Name field does not accept keyboard input. |
| BUG-007 | Order Completion | `error_user` | TC-ORDER-004 | Finish button does not respond, preventing order completion. |

## 3. Defect-to-Test Case Relationship

Each verified defect is directly associated with a failed test case.

| Test Case ID | Defect ID | Result |
|---|---|---|
| TC-PRODUCT-006 | BUG-001 | FAIL |
| TC-PRODUCT-007 | BUG-002 | FAIL |
| TC-DETAILS-004 | BUG-003 | FAIL |
| TC-CART-006 | BUG-004 | FAIL |
| TC-CHECKOUT-007 | BUG-005 | FAIL |
| TC-CHECKOUT-008 | BUG-006 | FAIL |
| TC-ORDER-004 | BUG-007 | FAIL |

This provides direct traceability between observed application failures and the corresponding defect records.

## 4. Defect Classification

The identified defects are concentrated in the following functional areas:

- Product image rendering
- Product sorting
- Product-to-details navigation
- Product interaction controls
- Checkout form behavior
- Order completion

The defects were observed while testing specific SauceDemo test personas and represent behavior that did not match the expected results defined in the corresponding test cases.

## 5. Defect Details

### BUG-001 — Incorrect Product Images

**Module:** Product Inventory  
**User:** `problem_user`  
**Related Test Case:** TC-PRODUCT-006  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
Each product should display the correct image corresponding to that product.

**Actual Result:**  
All products displayed the same incorrect dog image instead of their corresponding product images.

**Impact:**  
Incorrect product imagery can prevent users from reliably identifying products and reduces confidence in the product catalog.

---

### BUG-002 — Product Sorting Does Not Reorder Products

**Module:** Product Inventory  
**User:** `problem_user`  
**Related Test Case:** TC-PRODUCT-007  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
Selecting a sorting option should reorder the product list according to the selected criterion.

**Actual Result:**  
The sorting dropdown allowed the user to select different options, but the product list did not change or reorder.

**Impact:**  
Users cannot reliably organize or locate products using the available sorting functionality.

---

### BUG-003 — Incorrect Product Details Navigation

**Module:** Product Details  
**User:** `problem_user`  
**Related Test Case:** TC-DETAILS-004  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
Selecting a product should open the Product Details page for the selected product.

**Actual Result:**  
Product names opened mismatched Product Details pages. Selecting one product could display the details of a different product.

**Impact:**  
Users may view or purchase information for a product different from the one they selected.

---

### BUG-004 — Inconsistent Add to Cart / Remove Behavior

**Module:** Product Interaction  
**User:** `problem_user`  
**Related Test Case:** TC-CART-006  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
Selecting Add to Cart should add the selected product, change the control to Remove, and update the cart counter accordingly. Selecting Remove should remove the product and update the cart counter.

**Actual Result:**  
Certain products did not update their button state correctly, and adding or removing items caused inconsistencies in the cart counter.

**Impact:**  
Users may receive incorrect feedback about whether a product has been added to or removed from the cart.

**Clarification:**  
This defect concerns the **Add to Cart / Remove controls on the Products page** when using `problem_user`. It is categorized under Product Interaction because the incorrect behavior occurs on the Products page. The defect does not indicate that the Shopping Cart page itself failed.

---

### BUG-005 — Last Name Input Affects First Name Field

**Module:** Checkout  
**User:** `problem_user`  
**Related Test Case:** TC-CHECKOUT-007  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
Each checkout field should accept and retain only the value entered into that field.

**Actual Result:**  
While entering the Last Name, one character was also entered into the First Name field. Postal Code input worked as expected.

**Impact:**  
Incorrect field interaction can result in inaccurate customer information being submitted during checkout.

---

### BUG-006 — Last Name Field Does Not Accept Input

**Module:** Checkout  
**User:** `error_user`  
**Related Test Case:** TC-CHECKOUT-008  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
The Last Name field should accept valid keyboard input and retain the entered value. The checkout form should require valid required information before continuing.

**Actual Result:**  
The Last Name field did not accept keyboard input. Despite the missing Last Name value, clicking Continue still navigated to the Checkout Overview page.

**Impact:**  
Users may be unable to provide required checkout information, while the application may still allow the workflow to continue with incomplete data.

---

### BUG-007 — Finish Button Does Not Respond

**Module:** Order Completion  
**User:** `error_user`  
**Related Test Case:** TC-ORDER-004  
**Severity:** Medium  
**Status:** Open

**Expected Result:**  
Clicking Finish on the Checkout Overview page should complete the order and display the order confirmation page.

**Actual Result:**  
Clicking Finish had no effect and the Checkout Overview page remained displayed. The order was not completed.

**Impact:**  
The user cannot complete the purchase workflow using the affected test persona.

## 6. Important Clarification

The failed test cases represent situations where the application's actual behavior did not meet the expected result defined in the corresponding test cases.

Expected negative scenarios are not classified as defects when the application responds correctly.

For example:

- Invalid login credentials were rejected as expected.
- Blank required login fields were validated as expected.
- The locked-out user was prevented from logging in as expected.
- Missing checkout information was rejected as expected.

These scenarios were therefore recorded as **PASS**, not defects.

## 7. Defect Status

The defects listed in this folder were identified and verified during manual test execution.

Since the defects were not fixed and retested as part of this project, their current status is:

**Status: Open**


## 8. Defect Traceability Summary

The seven verified defects are directly traceable to the seven failed test cases identified during the final functional execution.

| Defect ID | Test Case | Requirement | Module |
|---|---|---|---|
| BUG-001 | TC-PRODUCT-006 | FR-PRODUCT-002 | Product Inventory |
| BUG-002 | TC-PRODUCT-007 | FR-PRODUCT-003 | Product Inventory |
| BUG-003 | TC-DETAILS-004 | FR-DETAILS-001 | Product Details |
| BUG-004 | TC-CART-006 | FR-CART-005 | Product Interaction |
| BUG-005 | TC-CHECKOUT-007 | FR-CHECKOUT-001 | Checkout |
| BUG-006 | TC-CHECKOUT-008 | FR-CHECKOUT-001 | Checkout |
| BUG-007 | TC-ORDER-004 | FR-ORDER-001 | Order Completion |

## 9. Conclusion

The defect documentation demonstrates the identification, verification, classification, and traceability of actual application failures during manual testing.

The project identified **7 verified defects across 37 executed test cases**.

Each failed test case is linked to a corresponding defect, while expected negative scenarios that behaved correctly were recorded as passing tests.

The identified defects should be investigated, fixed, and re-tested during a future regression cycle.
