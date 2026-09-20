# QA Engineering Portfolio

## Projects Overview

### 1. E2E Manual QA & Test Management — SauceDemo (Swag Labs)
* **Application Under Test:** SauceDemo (`https://www.saucedemo.com`)
* **Testing Scope:** End-to-End Manual Testing, Test Planning, Requirements Traceability, and Persona-Based Validation.
* **Key Deliverables & Execution:**
  * **Test Case Design & Execution:** Formulated and executed a comprehensive manual test suite covering **27 functional requirements and 37 detailed test cases** across core modules (Authentication, Product Inventory, Cart, Checkout, and Order Completion).
  * **Traceability Matrix:** Established a complete **Requirements Traceability Matrix (RTM)** to map business requirements to test scenarios, execution outcomes, and defect logs.
  * **Persona-Based Defect Discovery:** Leveraged application test personas (`standard_user`, `problem_user`, `error_user`) to identify, reproduce, and document **7 functional and UI defects** with full reproduction steps.
  * **Coverage:** Executed positive, negative, and edge-case End-to-End user workflows across varied user states.
* **Artifacts:**
  * [Test Plan & RTM Matrix](./project-1/test-plan-rtm.md)
  * [Defect Reports & Test Case Execution Logs](./project-1/)

### 2. REST API & Functional QA Project — Swagger Petstore
* **Application Under Test:** Swagger Petstore REST API (`https://petstore.swagger.io/v2`)
* **Testing Scope:** Functional REST API Validation, Schema Verification, Dynamic Data Chaining, and Integration Testing.
* **Key Deliverables & Execution:**
  * **Hybrid Test Suite:** Designed and executed a test suite comprising **19 test scenarios and 15 manual test cases** across the Pet, Store, and User modules.
  * **API Testing & Assertion:** Utilized **Postman** to validate HTTP response status codes (200, 404), JSON response schemas, and endpoint data persistence.
  * **E2E Data Chaining:** Implemented dynamic variable chaining to validate dependent API behavior in Pet Lifecycle workflows (Create → Retrieve → Update → Verify → Delete), achieving a **100% API pass rate**.
  * **Defect Lifecycle Management:** Uncovered and logged edge-case API behaviors (missing mandatory field handling, session behavior on invalid payload) as formal Jira defects (`SPQ-6`, `SPQ-7`).
* **Artifacts:**
  * [API Test Summary Report](./project-2/test-summary.md)
  * [Postman Collections & Environment Files](./project-2/)
  * [Jira Defect Logs](./Swagger-Petstore-QA-Portfolio/)

---

## Technical Competencies & Tooling

| Category | Skills & Tools |
| :--- | :--- |
| **API Testing** | Postman, REST API, JSON Schema Validation, Data Chaining, Environment Variables |
| **Test Design & Methodology** | Requirements Traceability Matrix (RTM), Test Case Design, Functional & E2E Testing, Persona Testing |
| **Defect Management** | Jira (Severity Classification, Root Cause Steps, Bug Reporting) |
| **Version Control & Docs** | Markdown, GitHub |
