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

### Expected Result

Invalid credentials should not result in a successful login response or
session token.

### Actual Result

The endpoint returned `200 OK` and a session token string despite the
invalid password.

### QA Note

This behavior was observed in the public Swagger Petstore mock environment
and may reflect the simplified behavior of the sandbox rather than a
production authentication implementation.


### Evidence

Jira issue: `SPQ-7`

Postman responses were used as test evidence.
