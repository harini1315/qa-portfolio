# Integration and End-to-End Test Report

## 1. Testing Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Tool | Postman |
| API Module | Pet API |
| Testing Types | Integration and End-to-End |
| Execution Status | Completed |
| Overall Result | **Passed** |

---

## 2. Purpose

This report summarizes the Integration and End-to-End testing performed against the Swagger Petstore Pet API.

The testing focused on validating data flow between dependent API requests and verifying the complete lifecycle of a Pet API resource.

---

# 3. Integration Testing

## 3.1 Integration Testing Objective

Integration testing was performed to verify that multiple Pet API operations work together correctly.

The integration workflow validates that a pet created through one API request can subsequently be retrieved, updated, and verified through other API requests.

---

## 3.2 Integration Workflow

```text
POST /pet
Create Pet
    ↓
GET /pet/{petId}
Retrieve Created Pet
    ↓
PUT /pet
Update Pet
    ↓
GET /pet/{petId}
Verify Updated Pet
