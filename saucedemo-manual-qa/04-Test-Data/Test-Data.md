# Test Data

## 1. Application

**Application:** SauceDemo / Swag Labs  
**URL:** https://www.saucedemo.com

## 2. User Credentials

SauceDemo provides multiple predefined test personas. These users were used during the overall manual testing activity to evaluate authentication, functional behavior, user-specific behavior, and different application conditions.

| Persona | Username | Password | Purpose |
|---|---|---|---|
| Standard User | `standard_user` | `secret_sauce` | Standard functional and end-to-end testing |
| Locked Out User | `locked_out_user` | `secret_sauce` | Authentication and access restriction testing |
| Problem User | `problem_user` | `secret_sauce` | User-specific functional behavior testing |
| Performance Glitch User | `performance_glitch_user` | `secret_sauce` | User-specific application behavior testing |
| Error User | `error_user` | `secret_sauce` | User-specific functional and error behavior testing |
| Visual User | `visual_user` | `secret_sauce` | User-specific visual and functional behavior testing |

## 3. Invalid Login Data

| Data | Value | Purpose |
|---|---|---|
| Invalid Username | `invalid_user` | Negative login testing |
| Invalid Password | `invalid_password` | Negative login testing |
| Blank Username | Empty | Required-field validation |
| Blank Password | Empty | Required-field validation |

## 4. Checkout Data

| Field | Test Value |
|---|---|
| First Name | QA |
| Last Name | Tester |
| Postal Code | 682001 |

The checkout values above were used as sample test data during manual execution.

## 5. Test Data Usage

The available SauceDemo test personas were used throughout the testing activity according to the scenarios being evaluated.

The testing included:

- Authentication and login validation
- Standard functional workflows
- Negative scenarios
- User-specific application behavior
- Product and shopping workflow validation
- Checkout and order completion
- Session and logout behavior
- Cross-module and end-to-end workflows

The formal test-case documentation represents the selected test scenarios used for structured test design, execution, traceability, and reporting. It does not necessarily represent every individual exploratory or supporting test action performed during the overall testing activity.

## 6. Defect-Related Test Data

User-specific testing resulted in verified failures associated with:

- `problem_user`
- `error_user`

These observations are documented in the relevant test cases and defect documentation.

No additional defect should be inferred solely from the presence of a test persona in the test data.

## 7. Test Data Management

The test data was selected to support positive, negative, restricted-user, user-specific, cross-module, and end-to-end testing.

Only actual observations from manual execution are used as formal test results and defect findings.

The same test data may be reused across multiple test cases where appropriate, while the test persona may vary depending on the scenario being evaluated.
