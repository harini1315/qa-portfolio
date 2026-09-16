# Regression Test Report

## 1. Regression Testing Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Testing Type | Regression Testing |
| Tool | Postman |
| API Module | Pet API |
| Execution Status | Completed |
| Overall Result | **Passed** |

---

## 2. Purpose

Regression testing was performed to verify that previously validated Pet API functionality continued to work correctly after changes to the pet data and API workflow.

The regression scope included the core Pet API operations and validation of both successful and expected error responses.

---

## 3. Regression Test Scope

The regression suite covered:

- Pet creation
- Pet retrieval
- Pet update
- Verification of updated pet data
- Pet deletion
- Verification of deleted pet
- HTTP status validation
- Response body validation
- Negative response validation
- Postman automated assertions

---

## 4. Regression Test Workflow

```text
Create Pet
    ↓
Retrieve Pet
    ↓
Update Pet
    ↓
Verify Updated Pet
    ↓
Delete Pet
    ↓
Verify Deletion
