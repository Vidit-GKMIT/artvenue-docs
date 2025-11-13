# ArtVenue – Unit Test Plan

## 1. Introduction

ArtVenue is a platform that connects **artists** with **venue owners**.  

## 2.Objective

The objective of this test plan is to ensure the ArtVenue platform meets all functional, non-functional, usability, and security requirements. The testing will validate:

- Smooth login/register of artists and venue owners.
- Venue listing, event creation, and artist opt-in workflows.
- Correct email notification system.
- Proper access control based on user roles (Artist / Venue Owner).

## 2. Scope of Testing

The objective of the Jest Test Plan is to ensure the correctness, reliability of the ArtVenue platform by thoroughly testing:

- User registration and authentication
- Artist and venue owner workflows
- Event creation and opt-in features
- OTP generation and validation
- Email notification system
- Backend service logic

### 2.1 Scope of Unit Testing

- Unit tests will cover:
- Utility functions (validators, formatters).
- Controllers (signup, login, venue creation, event creation).
- OTP generator (must generate 6-digit numeric only).
- Middleware (authentication, role-based access control).

## 3. Negative and Edge-Case Testing
- Missing fields
- Invalid OTP
- Duplicate opt-ins
- Unauthorized requests

## 4. Test Environment

Tests will be executed in the following environment:

- **Frontend:** Jest
- **Backend:** Jest  

## 5. User Register

| Test Case ID | Scenario | Input | Expected Output |
|--------------|----------|--------|-----------------|
| TC-01 | Register with valid artist data | name, email, password, role=artist, age and category | User created, directed to artist page |
| TC-02 | Register with valid venue owner data | name, email, password, role=owner | User created, directed to owner page|
| TC-03 | Register  field   | no name | Can't register |
| TC-04 | Unavailable email | email | Register button still disabled |
| TC-05 | Available email   | email | Register button enabled |
| TC-06 | Duplicate username | username | Username already registered |
| TC-07 | All input correct, invalid or expired OTP | OTP  |  Can't register  |

## 6. User Login 

| Test Case ID | Scenario | Input | Expected Output |
|--------------|----------|--------|-----------------|
| TC-01 | Login success | correct email/password | Redirect to profile page |
| TC-02 | Wrong password | existing email + wrong password or wrong email + existing email | Incorrect password |
| TC-03 | User not registered | unknown email | User not found |
| TC-04 | Missing credentials | empty email/password | Email & password required |

## 7. OTP Generation & Validation – Test Cases

| Test Case ID | Scenario | Input | Expected Output |
|--------------|----------|--------|-----------------|
| TC-01 | Generate OTP | call generateOTP() | OTP length must be exactly 6 |
| TC-02 | OTP must be a number type | output type | typeof OTP === "number" |
| TC-03 | Randomness check | call OTP multiple times | No two consecutive OTPs should be identical |
| TC-04 | Invalid OTP format | OTP less than 6 digits | Invalid OTP format |
| TC-05 | Expired OTP | OTP older than expiry time | OTP expired |