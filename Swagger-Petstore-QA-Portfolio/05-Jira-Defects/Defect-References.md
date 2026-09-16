# Jira Defect References

## SPQ-6 — Pet Creation Accepts Missing Required Name

| Field | Details |
|---|---|
| Jira Issue | `SPQ-6` |
| Summary | POST /pet accepts a pet without the required name field |
| Module | Pet |
| Endpoint | `POST /pet` |
| Severity | Medium |
| Priority | Medium |
| Status | To Do |
| Test Case | TC-PET-07 |

### Finding

The `POST /pet` endpoint accepted a request where the required top-level
`name` field was missing.

The API returned `200 OK` and created the pet.

A follow-up `GET /pet/123458` also returned `200 OK`, confirming that the
incomplete pet was persisted.

### Reproduction

The issue was reproduced with two different pet IDs:

- `123457`
- `123458`

Both requests were accepted without a pet `name`.

### Evidence

Jira issue: `SPQ-6`

Postman responses were used as test evidence.




## SPQ-7 — User Login Accepts Invalid Credentials

| Field | Details |
|---|---|
| Jira Issue | `SPQ-7` |
| Summary | GET /user/login accepts invalid credentials and returns successful login session |
| Module | User |
| Endpoint | `GET /user/login` |
| Severity | High |
| Priority | High |
| Status | To Do |
| Test Case | TC-USER-03 |


### Finding

The user login endpoint (`GET /user/login`) in this public mock sandbox environment acts as a simplified utility endpoint rather than a secure authentication gateway. When executing `TC-USER-03`, supplying an incorrect password for a registered username still returned a success status code and session token string.

### Reproduction

The behavior was observed using the following invalid credentials:
- Username: Valid registered user
- Invalid Passwords tested: `WrongPassword123`, `CompletelyWrong999`

Both requests returned `200 OK`. 

### Expected Result & QA Note

- In a production-grade application, the backend should validate passwords and return `400 Bad Request` or `401 Unauthorized` for invalid entries.
- In this public sandbox environment, this is recognized as an API mock environment limitation rather than a critical application security bug.

### Evidence

Jira issue: `SPQ-7`

Postman responses were used as test evidence.