# API Test Report

## API Testing Summary

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Tool | Postman |
| Environment | Swagger Petstore Environment |
| Base URL | `https://petstore.swagger.io/v2` |
| Primary API Tests | 6 |
| Passed | 6 |
| Failed | 0 |
| Blocked | 0 |
| Overall Result | **Passed** |

---

## API-01 — Create Pet

| Field | Details |
|---|---|
| API Test | `API-01` |
| Test Case | `TC-PET-01` |
| Method | `POST` |
| Endpoint | `/pet` |
| Purpose | Create a new pet using valid data |
| Expected Status | `200 OK` |
| Actual Status | `200 OK` |
| Pet ID | `123458` |
| Pet Name | `API-Portfolio-Pet` |
| Pet Status | `available` |
| Postman Assertions | `5/5 Passed` |
| Result | **Passed** |

---

## API-02 — Retrieve Pet

| Field | Details |
|---|---|
| API Test | `API-02` |
| Test Case | `TC-PET-02` |
| Method | `GET` |
| Endpoint | `/pet/123458` |
| Purpose | Retrieve an existing pet using a valid pet ID |
| Expected Status | `200 OK` |
| Actual Status | `200 OK` |
| Pet ID | `123458` |
| Pet Name | `API-Portfolio-Pet` |
| Pet Status | `available` |
| Postman Assertions | `5/5 Passed` |
| Result | **Passed** |

---

## API-03 — Update Pet

| Field | Details |
|---|---|
| API Test | `API-03` |
| Test Case | `TC-PET-03` |
| Method | `PUT` |
| Endpoint | `/pet` |
| Purpose | Update an existing pet |
| Expected Status | `200 OK` |
| Actual Status | `200 OK` |
| Pet ID | `123458` |
| Updated Name | `API-Portfolio-Pet-Updated` |
| Updated Status | `sold` |
| Postman Assertions | `5/5 Passed` |
| Result | **Passed** |

---

## API-04 — Verify Updated Pet

| Field | Details |
|---|---|
| API Test | `API-04` |
| Test Case | `TC-PET-04` |
| Method | `GET` |
| Endpoint | `/pet/123458` |
| Purpose | Verify that the updated pet data was persisted |
| Expected Status | `200 OK` |
| Actual Status | `200 OK` |
| Pet ID | `123458` |
| Verified Name | `API-Portfolio-Pet-Updated` |
| Verified Category | `Dog` |
| Verified Status | `sold` |
| Postman Assertions | `5/5 Passed` |
| Result | **Passed** |

---

## API-05 — Delete Pet

| Field | Details |
|---|---|
| API Test | `API-05` |
| Test Case | `TC-PET-05` |
| Method | `DELETE` |
| Endpoint | `/pet/123458` |
| Purpose | Delete an existing pet |
| Expected Status | `200 OK` |
| Actual Status | `200 OK` |
| Response Code | `200` |
| Deleted Pet ID | `123458` |
| Postman Assertions | `4/4 Passed` |
| Result | **Passed** |

---

## API-06 — Verify Deleted Pet

| Field | Details |
|---|---|
| API Test | `API-06` |
| Test Case | `TC-PET-06` |
| Method | `GET` |
| Endpoint | `/pet/123458` |
| Purpose | Verify that the deleted pet can no longer be retrieved |
| Expected Status | `404 Not Found` |
| Actual Status | `404 Not Found` |
| Error Code | `1` |
| Error Type | `error` |
| Error Message | `Pet not found` |
| Postman Assertions | `4/4 Passed` |
| Result | **Passed** |

---

## API Workflow

```text
TC-PET-01
POST /pet
Create Pet
    ↓
TC-PET-03
GET /pet/123458
Retrieve Pet
    ↓
TC-PET-04
PUT /pet
Update Pet
    ↓
TC-PET-03
GET /pet/123458
Verify Update
    ↓
TC-PET-05
DELETE /pet/123458
Delete Pet
    ↓
TC-PET-03
GET /pet/123458
Verify Deletion
