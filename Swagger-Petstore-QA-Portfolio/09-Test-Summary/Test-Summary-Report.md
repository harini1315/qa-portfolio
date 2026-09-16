# Test Summary Report

## 1. Project Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Testing Scope | Manual Functional, API, Integration and Pet Lifecycle E2E |
| Primary Testing Tool | Postman |
| Defect Tracking | Jira |
| API Base URL | `https://petstore.swagger.io/v2` |
| Execution Status | Completed |
| Overall QA Result | **Passed with Known Defects** |

This report provides the final summary of the QA activities performed for the Swagger Petstore QA Portfolio.

The testing covered the Pet, Store, and User modules, including positive and negative functional scenarios, REST API validation, API data chaining, Integration testing, Pet Lifecycle E2E testing, defect identification, and test reporting.

---

## 2. Testing Scope

The project included the following QA activities:

- Requirements analysis
- Test planning
- Manual functional testing
- Positive testing
- Negative testing
- REST API testing
- API response validation
- Postman test scripts and assertions
- API data chaining
- Integration testing
- Pet Lifecycle E2E testing
- Smoke testing
- Regression testing
- Defect identification
- Jira defect documentation
- Test execution reporting
- QA metrics
- Final test summary

---

## 3. Application Areas Tested

| Module | Functional Areas Covered |
|---|---|
| Pet | Create, Retrieve, Find by Status, Update, Delete, Negative validation |
| Store | Inventory retrieval, Order creation, Order retrieval, Order deletion, Negative order retrieval |
| User | User creation, Login, Invalid login |
| Pet Lifecycle | Create → Update → Verify → Delete → Verify Deletion |

---

## 4. Test Execution Summary

| Testing Type | Total | Passed | Failed | Blocked | Pass Rate |
|---|---:|---:|---:|---:|---:|
| Manual Functional Testing | 15 | 13 | 2 | 0 | **86.67%** |
| API Testing | 6 | 6 | 0 | 0 | **100%** |
| Integration Testing | 4 | 4 | 0 | 0 | **100%** |
| Pet Lifecycle E2E Testing | 5 | 5 | 0 | 0 | **100%** |

> Negative scenarios are included within the Manual and API testing coverage rather than being counted as a separate testing level.

No tests were blocked or left unexecuted within the documented testing scope.

---

## 5. Manual Functional Testing

Manual testing covered the Pet, Store, and User modules.

| Module | Total | Passed | Failed | Pass Rate |
|---|---:|---:|---:|---:|
| Pet | 7 | 6 | 1 | 85.71% |
| Store | 5 | 5 | 0 | 100.00% |
| User | 3 | 2 | 1 | 66.67% |
| **Total** | **15** | **13** | **2** | **86.67%** |

The two failed scenarios were:

- `TC-PET-07` — Pet creation accepted a request without the mandatory `name` field.
- `TC-USER-03` — Login accepted invalid passwords and returned a successful session response.

---

## 6. API Testing

API testing was performed using Postman against the Swagger Petstore REST API.

The API workflow covered:

```text
POST /pet
Create Pet
    ↓
GET /pet/{petId}
Retrieve Pet
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
