---
title: Login Functionality
id: TC-001
component: Authentication
priority: High
status: Active
tags:
  - smoke-test
  - regression
last_updated: 2024-12-24
---

# Login Functionality Test Cases

## TC-001: Standard User Login

### Test Objective
Verify that a user can successfully log in with valid credentials

### Prerequisites
1. User has a valid account
2. User is not currently logged in
3. System is accessible

### Test Steps

| Step | Action | Expected Result | Test Data |
|------|--------|----------------|------------|
| 1 | Navigate to login page | Login form is displayed | N/A |
| 2 | Enter valid username | Username is accepted | user@example.com |
| 3 | Enter valid password | Password field shows dots | Password123! |
| 4 | Click login button | User is successfully logged in | N/A |

### Post-conditions
- User is logged in
- User is redirected to dashboard
- Session is created

### Notes
- Test on supported browsers: Chrome, Firefox, Safari
- Check "Remember me" functionality in separate test case

## TC-002: Invalid Login Attempt

=== "Test Steps"
    | Step | Action | Expected Result | Test Data |
    |------|--------|----------------|------------|
    | 1 | Navigate to login page | Login form is displayed | N/A |
    | 2 | Enter invalid username | Username is accepted | invalid@example.com |
    | 3 | Enter invalid password | Password field shows dots | wrongpass123 |
    | 4 | Click login button | Error message displayed | N/A |

=== "Expected Results"
    - Error message: "Invalid username or password"
    - User remains on login page
    - No session created

=== "Test Data"
    ```json
    {
      "invalid_credentials": {
        "username": "invalid@example.com",
        "password": "wrongpass123"
      }
    }
    ```
