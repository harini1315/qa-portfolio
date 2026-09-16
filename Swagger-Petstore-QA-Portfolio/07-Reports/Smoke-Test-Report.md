# Smoke Test Report

## 1. Smoke Testing Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Testing Type | Smoke Testing |
| Tool | Postman |
| API Module | Pet API |
| Execution Status | Completed |
| Overall Result | **Passed** |

---

## 2. Purpose

Smoke testing was performed to verify that the critical Pet API functionality was available and responding correctly before broader API and workflow validation.

The smoke test focused on the core API operations required to confirm that the Pet API was functional.

---

## 3. Smoke Test Scope

The following critical operations were selected:

- Create Pet
- Retrieve Pet
- Update Pet
- Verify Updated Pet
- Delete Pet
- Verify Deleted Pet

These tests provide a quick validation of the primary Pet API lifecycle.

---

## 4. Smoke Test Workflow

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
    ↓
404 Not Found
