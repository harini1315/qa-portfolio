# Test Scenarios

## 1. Purpose

These test scenarios define the main areas of functionality that will be tested in the Swagger Petstore application.

The scenarios are based on the functional requirements identified in the requirements document.

## 2. Test Scenarios

| Scenario ID | Requirement ID | Module | Test Scenario | Priority |
|---|---|---|---|---|
| TS-PET-01 | FR-PET-01 | Pet | Verify that a new pet can be created with valid details. | High |
| TS-PET-02 | FR-PET-02 | Pet | Verify that pet details can be retrieved using a valid pet ID. | High |
| TS-PET-03 | FR-PET-03 | Pet | Verify that pets can be filtered by available, pending, and sold status. | Medium |
| TS-PET-04 | FR-PET-04 | Pet | Verify that existing pet details can be updated. | High |
| TS-PET-05 | FR-PET-05 | Pet | Verify that an existing pet can be deleted. | High |
| TS-STORE-01 | FR-STORE-01 | Store | Verify that current inventory information can be retrieved. | Medium |
| TS-STORE-02 | FR-STORE-02 | Store | Verify that an order can be created for an existing pet. | High |
| TS-STORE-03 | FR-STORE-03 | Store | Verify that an existing order can be retrieved using its order ID. | High |
| TS-STORE-04 | FR-STORE-04 | Store | Verify that an existing order can be deleted. | Medium |
| TS-USER-01 | FR-USER-01 | User | Verify that a new user can be created with valid details. | Medium |
| TS-USER-02 | FR-USER-02 | User | Verify that a registered user can log in with valid credentials. | High |
| TS-USER-03 | FR-USER-03 | User | Verify that a logged-in user can log out successfully. | Medium |

## 3. Negative Testing Scenarios

The following negative scenarios will also be covered within the above functional areas:

| Scenario ID | Module | Negative Scenario |
|---|---|---|
| TS-NEG-01 | Pet | Verify the response when a non-existent pet ID is requested. |
| TS-NEG-02 | Pet | Verify how the API handles incomplete or invalid pet data. |
| TS-NEG-03 | Store | Verify how the API handles invalid order information. |
| TS-NEG-04 | Store | Verify the response when a non-existent order ID is requested. |
| TS-NEG-05 | User | Verify login behavior with invalid credentials. |

## 4. Integration and End-to-End Scenarios

| Scenario ID | Modules | Test Scenario |
|---|---|---|
| TS-E2E-01 | Pet + Store | Create a pet, place an order for that pet, and verify the order details. |
| TS-E2E-02 | Pet + Store | Create a pet, update its details, and verify the updated information before using it in an order. |

## 5. Scenario to Test Case Mapping

The scenarios above will be converted into 15 detailed manual test cases in the next step.

The planned relationship is:

```text
Functional Requirement
        ↓
Test Scenario
        ↓
Manual Test Case
        ↓
Test Execution
        ↓
Defect (if applicable)
