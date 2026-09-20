# QA Engineering Portfolio

## Projects Overview

### 1. E2E Manual QA & Test Management — SauceDemo (Swag Labs)

* **Application Under Test:** SauceDemo (`https://www.saucedemo.com`)
* **Testing Scope:** End-to-End Manual Testing, Test Planning, Requirements Traceability, and Persona-Based Validation.
* **Key Deliverables & Execution:**
  * **Test Case Design & Execution:** Designed and executed a comprehensive manual test suite covering **27 functional requirements and 37 detailed test cases** across core modules (Authentication, Product Inventory, Cart, Checkout, and Order Completion).
  * **Traceability Matrix:** Established a complete **Requirements Traceability Matrix (RTM)** to map requirements to test scenarios, execution outcomes, and defect logs.
  * **Persona-Based Defect Discovery:** Leveraged application test personas (`standard_user`, `problem_user`, `error_user`) to identify, reproduce, and document **7 functional and UI defects** with detailed reproduction steps.
  * **Coverage:** Executed positive, negative, and edge-case End-to-End user workflows across varied user states.
* **Artifacts:**
  * [Test Plan & RTM Matrix](./saucedemo-manual-qa/test-plan-rtm.md)
  * [Defect Reports & Test Case Execution Logs](./saucedemo-manual-qa/)

### 2. REST API & Functional QA Project — Swagger Petstore

* **Application Under Test:** Swagger Petstore REST API (`https://petstore.swagger.io/v2`)
* **Testing Scope:** Functional REST API Testing, Response Data Validation, Data Chaining, and Integration Testing.
* **Key Deliverables & Execution:**
  * **Hybrid Test Suite:** Designed and executed a test suite comprising **19 test scenarios and 15 manual test cases** across the Pet, Store, and User modules.
  * **API Testing:** Utilized **Postman** to validate HTTP response status codes (200, 404), response data, and endpoint behavior.
  * **Integration & E2E Validation:** Validated API workflows through Integration and End-to-End testing using Create → Retrieve → Update → Verify → Delete operations, checking response data and expected behavior across dependent requests.
  * **Defect Management:** Identified and documented functional and data-handling defects in **Jira**, including missing mandatory fields and incorrect payload behavior, with clear reproduction steps and expected versus actual results.
* **Artifacts:**
  * [API Test Summary Report](./Swagger-Petstore-QA-Portfolio/09-test-Summary.md)
  * [Postman Collections & Environment Files](./Swagger-Petstore-QA-Portfolio/)
  * [Jira Defect Logs](./Swagger-Petstore-QA-Portfolio/)

---

## Technical Competencies & Tooling

| Category | Skills & Tools |
| :--- | :--- |
| **API Testing** | Postman, REST API, Response Data Validation, Data Chaining, Environment Variables |
| **Test Design & Methodology** | Requirements Traceability Matrix (RTM), Test Case Design, Functional & E2E Testing, Persona Testing |
| **Defect Management** | Jira, Severity Classification, Bug Reporting |
| **Version Control & Documentation** | Markdown, GitHub |
