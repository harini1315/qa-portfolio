# Test Execution Report

## 1. Test Execution Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Testing Type | Functional, API, Integration and End-to-End |
| Primary Tool | Postman |
| API Base URL | `https://petstore.swagger.io/v2` |
| Execution Status | Completed |
| Overall Result | **Passed with Known Defects** |

---

## 2. Test Execution Scope

The test execution covered functional validation of the Swagger Petstore application and API.

The executed scope included:

- Manual functional testing
- REST API testing
- Positive API testing
- Negative API testing
- API response validation
- Postman automated assertions
- API integration workflow validation
- Pet lifecycle / E2E workflow validation
- Defect identification and documentation

---

## 3. Execution Summary

| Testing Area | Test Cases / Scenarios | Passed | Failed | Blocked | Result |
|---|---:|---:|---:|---:|---|
| Manual Testing | 15 | 13 | 2 | 0 | **Passed with Known Defects** |
| API Testing | 6 | 6 | 0 | 0 | **Passed** |
| Integration Testing | 4 | 4 | 0 | 0 | **Passed** |
| E2E Testing | 5 | 5 | 0 | 0 | **Passed** |

> Manual testing execution details are maintained in the Manual Test Cases and Test Planning documentation. API, Integration, and E2E execution results are supported by Postman assertions.

---

## 4. API Test Execution

The API tests were executed using Postman against the Swagger Petstore REST API.

### API Execution Results

| Test Case | Method | Endpoint | Expected | Actual | Result |
|---|---|---|---|---|---|
| `TC-PET-01` | POST | `/pet` | `200 OK` | `200 OK` | **Passed** |
| `TC-PET-02` | GET | `/pet/{petId}` | `200 OK` | `200 OK` | **Passed** |
| `TC-PET-03` | PUT | `/pet` | `200 OK` | `200 OK` | **Passed** |
| `TC-PET-04` | GET | `/pet/{petId}` | `200 OK` | `200 OK` | **Passed** |
| `TC-PET-05` | DELETE | `/pet/{petId}` | `200 OK` | `200 OK` | **Passed** |
| `TC-PET-06` | GET | `/pet/{petId}` | `404 Not Found` | `404 Not Found` | **Passed** |

### API Execution Result

- Total API test cases: **6**
- Passed: **6**
- Failed: **0**
- Blocked: **0**
- Pass Rate: **100%**

---

## 5. API Assertion Results

Postman Post-response scripts were used to validate the API responses.

### Create Pet

Assertions validated:

- Status code is `200`
- Created pet ID
- Created pet name
- Created pet category
- Created pet status

**Result: 5/5 Passed**

### Retrieve Pet

Assertions validated:

- Status code is `200`
- Retrieved pet ID
- Retrieved pet name
- Retrieved pet category
- Retrieved pet status

**Result: 5/5 Passed**

### Update Pet

Assertions validated:

- Status code is `200`
- Updated pet ID
- Updated pet name
- Updated pet category
- Updated pet status

**Result: 5/5 Passed**

### Verify Updated Pet

Assertions validated:

- Status code is `200`
- Verified pet ID
- Verified updated pet name
- Verified pet category
- Verified updated pet status

**Result: 5/5 Passed**

### Delete Pet

Assertions validated:

- Status code is `200`
- Deleted pet ID
- Delete response code
- Delete response type
- Delete response message

**Result: 5/5 Passed**

### Verify Deleted Pet

Assertions validated:

- Status code is `404`
- Error code is `1`
- Error type is `error`
- Error message is `Pet not found`

**Result: 4/4 Passed**

---

### Integration Execution Result

| Metric | Result |
|---|---:|
| Total Integration Tests | 4 |
| Passed | 4 |
| Failed | 0 |
| Blocked | 0 |
| Pass Rate | **100%** |

The integration workflow confirmed that the Pet created in the first request could be retrieved, updated, and subsequently verified using the dependent API requests.

---

## 7. Pet Lifecycle E2E Test Execution

The Pet Lifecycle E2E workflow validated the complete lifecycle of a Pet resource.

### E2E Workflow

```text
POST /pet
Create Pet
    ↓
PUT /pet
Update Pet
    ↓
GET /pet/{petId}
Verify Updated Pet
    ↓
DELETE /pet/{petId}
Delete Pet
    ↓
GET /pet/{petId}
Verify Deletion
    ↓
Expected: 404 Not Found ✓



