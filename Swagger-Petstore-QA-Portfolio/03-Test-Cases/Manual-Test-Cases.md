# Manual Test Cases

## 1. Test Case Information

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Testing Type | Manual Functional Testing |
| Total Test Cases | 15 |
| Test Environment | Swagger Petstore API |
| Status | Execution Completed |


## 2. Test Case Format

The test cases below cover the main Pet, Store, and User functionality identified during requirements and test scenario analysis.

Actual results and execution status were recorded during manual test execution.


## 3. Pet Test Cases

| Test Case ID | Requirement ID | Scenario ID | Test Case | Preconditions | Test Data / Action | Expected Result | Actual Result | Status | Defect ID |
|---|---|---|---|---|---|---|---|---|---|
| TC-PET-01 | FR-PET-01 | TS-PET-01 | Create a new pet with valid details | Swagger Petstore API is available | Send `POST /pet` with `id: 0`, name `Rex`, and status `available` | Response is successful and contains the created pet with a unique pet ID | `200 OK` returned with pet ID `9223372036854775807`; response contained name `Rex` and status `available` | **Passed** | — |
| TC-PET-02 | FR-PET-02 | TS-PET-02 | Retrieve an existing pet using a valid pet ID | A pet exists with a valid pet ID | Send `GET /pet/123456` using the pet created during the controlled test | Response is successful and returns the correct pet details | `200 OK` returned pet ID `123456` with name `Rex` and status `available`, matching the pet data used in the controlled creation test | **Passed** | — |
| TC-PET-03 | FR-PET-03 | TS-PET-03 | Find pets by status | Swagger Petstore API is available | Send `GET /pet/findByStatus` with query parameter `status=available` | Response is successful and returns pets with `available` status | `200 OK` returned a list of pets containing records with `status: available` | **Passed** | — |
| TC-PET-04 | FR-PET-04 | TS-PET-04 | Update an existing pet's name and status | Pet with ID `123456` exists | Send `PUT /pet` with pet ID `123456` and change status from `available` to `sold` | Response is successful and the pet details reflect the update | `200 OK` returned the updated pet with ID `123456`, name `Rex`, and status `sold`. A follow-up `GET /pet/123456` confirmed the updated status was persisted | **Passed** | — |
| TC-PET-05 | FR-PET-05 | TS-PET-05 | Delete an existing pet | Pet with ID `123456` exists | Send `DELETE /pet/123456` | Response confirms successful deletion and the pet is no longer retrievable | `200 OK` returned with message `123456`. A follow-up `GET /pet/123456` returned `404 Not Found` with message `Pet not found`, confirming deletion | **Passed** | — |
| TC-PET-06 | FR-PET-02 | TS-NEG-01 | Retrieve a pet using a non-existent or deleted pet ID | Pet ID `123456` has been deleted | Send `GET /pet/123456` | API should return `404 Not Found` with an appropriate error message | `404 Not Found` returned with `code: 1`, `type: error`, and message `Pet not found` | **Passed** | — |
| TC-PET-07 | FR-PET-01 | TS-NEG-02 | Create a pet with missing mandatory name | Swagger Petstore API is available | Send `POST /pet` with valid pet data but omit the required top-level `name` field | API should reject the invalid request instead of creating a pet without a name | `200 OK` returned and pet ID `123458` was created without a top-level `name`. A follow-up `GET /pet/123458` also returned `200 OK`, confirming the incomplete pet was persisted | **Failed** | SPQ-6 |


### TC-PET-07 Investigation Note

The Swagger Petstore API definition identifies the Pet `name` field as required.
However, the API accepted the request without `name` and persisted the pet.

This behavior is being treated as a potential defect and will be verified
before creating a Jira issue.


### Execution Note

During execution, the API returned the maximum signed 64-bit integer
(`9223372036854775807`) when `id: 0` was supplied in the create-pet request.
A controlled test using explicit ID `123456` was performed to verify normal
create and retrieve behavior. The pet was successfully retrieved with
matching details.

No defect was logged from this observation.




## 4. Store Test Cases

| Test Case ID | Requirement ID | Scenario ID | Test Case | Preconditions | Test Data / Action | Expected Result | Actual Result | Status | Defect ID |
|---|---|---|---|---|---|---|---|---|---|
| TC-STORE-01 | FR-STORE-01 | TS-STORE-01 | Retrieve store inventory | API is available | Send `GET /store/inventory` | Response is successful and returns inventory counts grouped by status | `200 OK` returned an inventory object containing counts for `available`, `pending`, and `sold` statuses. The response also contained additional status-like keys. | **Passed** | — |
| TC-STORE-02 | FR-STORE-02 | TS-STORE-02 | Create an order for an existing pet | A valid pet ID exists | Send `POST /store/order` with valid pet ID `123456`, quantity `1`, and valid order details | Response is successful and returns the created order with an order ID | `200 OK` returned a created order with ID `9223372036854280695`, `petId: 123456`, quantity `1`, status `placed`, and `complete: false` | **Passed** | — |
| TC-STORE-03 | FR-STORE-03 | TS-STORE-03 | Retrieve an existing order | A valid order ID exists | Send `GET /store/order/9223372036854280695` using the order created during TC-STORE-02 | Response is successful and returns the correct order details | `200 OK` returned order ID `9223372036854280695` with `petId: 123456`, quantity `1`, status `placed`, and `complete: false`, matching the order created in TC-STORE-02 | **Passed** | — |
| TC-STORE-04 | FR-STORE-04 | TS-STORE-04 | Delete an existing order | An existing order ID is available | Send `DELETE /store/order/9223372036854280695` | Response confirms successful deletion | `200 OK` returned with the deleted order ID. A follow-up `GET /store/order/9223372036854280695` returned `404 Not Found` with message `Order not found`, confirming the order was deleted | **Passed** | — |
| TC-STORE-05 | FR-STORE-03 | TS-NEG-04 | Retrieve an order using a non-existent order ID | API is available | Send `GET /store/order/999999999` using a non-existent order ID | API returns the expected error response for a missing order | `404 Not Found` returned with `code: 1`, `type: error`, and message `Order not found` | **Passed** | — |


## 5. User Test Cases

| Test Case ID | Requirement ID | Scenario ID | Test Case | Preconditions | Test Data / Action | Expected Result | Actual Result | Status | Defect ID |
|---|---|---|---|---|---|---|---|---|---|
| TC-USER-01 | FR-USER-01 | TS-USER-01 | Create a new user with valid details | API is available | Send `POST /user` with valid user information using username `qa_user_100001` and user ID `100001` | Response is successful and the user is created | `200 OK` returned with `code: 200`, `type: unknown`, and message `100001`, indicating successful user creation | **Passed** | — |
| TC-USER-02 | FR-USER-02 | TS-USER-02 | Log in using valid user credentials | A valid user exists | Send `GET /user/login` with username `qa_user_100001` and valid password | Response is successful and returns a login confirmation/session message | `200 OK` returned with `code: 200` and message `logged in user session:1788088614643`, confirming successful login | **Passed** | — |
| TC-USER-03 | FR-USER-02 | TS-NEG-05 | Log in using invalid user credentials | API is available | Send `GET /user/login` with valid username `qa_user_100001` and invalid passwords | API returns an appropriate response indicating that login was not successful | `200 OK` returned with a successful login session message for invalid password `WrongPassword123`. The test was reproduced with a second invalid password `CompletelyWrong999`, which also returned `200 OK` with a login session message | **Failed** | SPQ-7 |



## 6. Test Case Summary

| Module | Test Cases |
|---|---:|
| Pet | 7 |
| Store | 5 |
| User | 3 |
| **Total** | **15** |



## 7. Execution Status

Manual execution of all 15 test cases has been completed.

| Status | Count |
|---|---:|
| Passed | 13 |
| Failed | 2 |
| Blocked | 0 |
| Not Executed | 0 |
| **Total** | **15** |

The two failed test cases were linked to genuine Jira defects:

- `TC-PET-07` → `SPQ-6`
- `TC-USER-03` → `SPQ-7`

All results are based on actual Postman execution and observed API responses.

