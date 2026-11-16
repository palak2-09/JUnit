# User Registration Validation System

## Project Overview

This project implements a User Registration Validation System using Java. It ensures that user details meet predefined validation requirements before registration is considered successful.

The system applies Regular Expressions (Regex) to validate user information, including names, email addresses, mobile numbers and passwords. JUnit 5 is integrated to test the validation logic and ensure that the application handles both acceptable and unacceptable inputs correctly.

The assignment is divided into 11 use cases, covering basic field validation, password security rules, email samples, and different JUnit testing techniques.

## Project Goals

- Develop reusable validation methods for user registration fields.
- Apply Regex patterns to enforce input validation rules.
- Verify validation methods through JUnit 5 test cases.
- Identify incorrect inputs using negative test scenarios.
- Implement parameterized testing for multiple email formats.
- Maintain separate feature branches for individual use cases.
- Follow a structured Git workflow for version control.

## Technology Stack

| Technology | Purpose |
|---|---|
| Java | Application development |
| Maven | Project and dependency management |
| JUnit 5 | Unit testing framework |
| Regex | Input pattern validation |
| Git & GitHub | Version control and branch management |
| IntelliJ IDEA | Development environment |

## Implementation Breakdown

The project consists of the following 11 use cases:

| Use Case | Feature | Validation Details |
|---|---|---|
| UC1 | First Name | Validates that the first name begins with an uppercase letter and has at least 3 characters. |
| UC2 | Last Name | Applies the required capitalization and minimum length conditions to the last name. |
| UC3 | Email Address | Checks email structure using mandatory and optional components. |
| UC4 | Mobile Number | Validates the country code, space separator and 10-digit mobile number. |
| UC5 | Password Length | Ensures that the password contains at least 8 characters. |
| UC6 | Uppercase Requirement | Checks whether the password contains at least one uppercase letter. |
| UC7 | Numeric Requirement | Ensures that the password includes at least one digit. |
| UC8 | Special Character Requirement | Checks for exactly one special character while satisfying the other password conditions. |
| UC9 | Email Samples | Tests the email validation logic against the provided sample email addresses. |
| UC10 | Happy and Sad Tests | Verifies successful and unsuccessful validation scenarios using JUnit 5. |
| UC11 | Parameterized Email Testing | Uses parameterized JUnit tests to execute email validation against multiple inputs. |

## Testing Strategy

JUnit 5 is used to check the correctness and reliability of the validation methods.

### 1. Positive Testing (Happy Path)

Tests are designed with valid inputs to confirm that the validation methods return the expected successful result.

### 2. Negative Testing (Sad Path)

Invalid inputs are supplied to ensure that incorrect registration details are rejected.

Examples include:
- Names beginning with lowercase letters.
- Names containing fewer than the required characters.
- Emails with invalid formats.
- Mobile numbers with incorrect formatting.
- Passwords missing mandatory conditions.

### 3. Parameterized Testing

Parameterized tests are used to execute the same validation method with different email inputs. This helps verify multiple test scenarios without writing separate test methods for every input.

## Project Directory Structure

The application follows the standard Maven project organization, keeping application classes and test classes in separate directories.

```text
JUnit/
│
├── README.md
├── pom.xml
│
└── src/
    │
    ├── main/
    │   └── java/
    │       └── registration/
    │           └── UserRegistration.java
    │
    └── test/
        └── java/
            └── registration/
                ├── UserRegistrationTest.java
                └── EmailValidationParameterizedTest.java
```

## Git Branching Strategy

Git branching is used to organize development and maintain individual use cases separately.

- **main:** Contains the stable project baseline.
- **develop:** Serves as the integration branch.
- **feature branches:** Each use case is developed independently before integration.

Feature branches follow this naming convention:

```text
feature/UC1-FirstName
feature/UC2-LastName
feature/UC3-Email
feature/UC4-Mobile
feature/UC5-PasswordLength
feature/UC6-Uppercase
feature/UC7-Number
feature/UC8-SpecialChar
feature/UC9-EmailSamples
feature/UC10-HappySadTests
feature/UC11-ParameterizedEmail
```

## Conclusion

This project demonstrates how Java Regex and JUnit 5 can be combined to build and test a reliable user registration validation system. It provides practical experience with input validation, unit testing, parameterized testing, Maven project management and Git-based development workflows.
