# Question 2: Login System – Test Case Design (10 Marks)

The following test cases cover successful authentication, input validation, incorrect credentials, and account lockout behavior.

| Test Case ID | Test Scenario | Test Input | Expected Result |
|---|---|---|---|
| HT_01 | Verify login with valid credentials | User ID: user1<br>Password: abc123 | User should be authenticated successfully and shown a login success message. |
| HT_02 | Verify login with username left blank | User ID: Blank<br>Password: abc123 | System should display "Username is required." |
| HT_03 | Verify login with password left blank | User ID: user1<br>Password: Blank | System should display "Password is required." |
| HT_04 | Verify password length validation for fewer than six characters | User ID: user1<br>Password: abc12 | System should display "Password must be at least 6 characters long." |
| HT_05 | Verify password at the minimum allowed length | User ID: user1<br>Password: abc123 | System should accept the password length and allow successful login. |
| HT_06 | Verify authentication with an unregistered username | User ID: unknownuser<br>Password: abc123 | System should display "Invalid username or password." |
| HT_07 | Verify authentication with an incorrect password | User ID: user1<br>Password: wrong123 | System should display "Invalid username or password." |
| HT_08 | Verify account lock after three consecutive unsuccessful login attempts | User ID: user1<br>Password: wrong123<br>Submit three consecutive times | First two attempts should show invalid credentials. The third unsuccessful attempt should lock the account. |
| HT_09 | Verify login attempt after account lockout | User ID: user1<br>Password: abc123 | System should display "Your account is locked. Please contact support." |

## Conclusion

These test cases cover the main login validation conditions, including valid credentials, empty fields, password length restrictions, invalid credentials, repeated failed attempts, and account lockout. They help verify that the login system handles authentication and security conditions as expected.