# Integration and End-to-End Test Cases

## Testing Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Tool | Postman |
| API Type | REST API |
| Testing Scope | API Integration and End-to-End Workflow Validation |
| Primary Module | Pet API |
| Automation | Postman Post-response Scripts |
| Positive Testing | Covered |
| Negative Testing | Covered |

---

# Integration Testing

## Integration Testing Context

Integration testing verifies that multiple API operations work together correctly and that data created or modified by one API request can be successfully consumed and validated by subsequent requests.

For this project, the integration workflow focuses on the Pet API and validates the dependency between Create, Retrieve, Update, and Verify operations.

The workflow demonstrates that:

- A pet can be created successfully.
- The created pet can be retrieved using its ID.
- The same pet can be updated.
- The updated information can be retrieved and verified.
- Data remains consistent across dependent API requests.

---

## Integration Workflow

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
