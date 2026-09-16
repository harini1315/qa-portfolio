# API Test Cases

## API Testing Overview

| Field | Details |
|---|---|
| Application | Swagger Petstore |
| Tool | Postman |
| Base URL | `https://petstore.swagger.io/v2` |
| Testing Type | REST API Testing |
| API Operations Covered | 5 |
| Test Cases | 6 |
| Test Types | Positive and Negative |
| Automation | Postman Post-response Scripts |

---

## API Test Case Summary

| Test Case ID | API Operation | Method | Endpoint | Test Type | Result |
|---|---|---|---|---|---|
| `TC-PET-01` | Create Pet | `POST` | `/pet` | Positive | **Passed** |
| `TC-PET-02` | Retrieve Pet | `GET` | `/pet/{petId}` | Positive | **Passed** |
| `TC-PET-03` | Update Pet | `PUT` | `/pet` | Positive | **Passed** |
| `TC-PET-04` | Verify Updated Pet | `GET` | `/pet/{petId}` | Positive | **Passed** |
| `TC-PET-05` | Delete Pet | `DELETE` | `/pet/{petId}` | Positive | **Passed** |
| `TC-PET-06` | Verify Deleted Pet | `GET` | `/pet/{petId}` | Negative | **Passed** |

---

## TC-PET-01 — Create Pet

| Field | Details |
|---|---|
| Test Case ID | `TC-PET-01` |
| Test Scenario | Create a new pet using valid data |
| Method | `POST` |
| Endpoint | `/pet` |
| Test Type | Positive |
| Priority | High |

### Preconditions

- Swagger Petstore API is accessible.
- Postman environment is configured.
- Valid pet data is available.

### Test Data

```json
{
    "id": 123458,
    "category": {
        "id": 1,
        "name": "Dog"
    },
    "name": "API-Portfolio-Pet",
    "photoUrls": [
        "https://example.com/api-portfolio-pet.jpg"
    ],
    "tags": [
        {
            "id": 1,
            "name": "API-Portfolio"
        }
    ],
    "status": "available"
}
