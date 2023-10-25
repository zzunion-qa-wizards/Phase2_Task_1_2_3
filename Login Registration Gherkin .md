# Login/Registration

# Gherkin GUI Test Cases

## Feature: Login/Registration in Metabase

```jsx
BackgroundLogin/Registration
```

```jsx
Feature: User Login
  Scenario: Login with Incorrect Username
    Given the user is not logged in
    When they enter an incorrect username and a valid password
    Then an error message is expected
    And the user receives an error message indicating an invalid username
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login with Incorrect Password
    Given the user is not logged in
    When they enter a valid username and an incorrect password
    Then an error message is expected
    And the user receives an error message indicating an incorrect password
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login with Empty Fields
    Given the user is not logged in
    When they leave both username and password fields empty
    Then an error message is expected
    And the user receives an error message indicating that both fields are required
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login with a Locked Account
    Given the user is not logged in
    When they enter a valid username and password for a locked account
    Then an error message is expected
    And the user receives an error message indicating that the account is locked
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login with a Non-existent Username
    Given the user is not logged in
    When they enter a username that doesn't exist in the system
    Then an error message is expected
    And the user receives an error message indicating that the username doesn't exist
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login with an Empty Username
    Given the user is not logged in
    When they enter an empty username and a valid password
    Then an error message is expected
    And the user receives an error message indicating an empty username
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login with an Empty Password
    Given the user is not logged in
    When they enter a valid username and an empty password
    Then an error message is expected
    And the user receives an error message indicating an empty password
    And the user is still on the login page
```

```jsx
Feature: User Login
  Scenario: Login Using a Password Manager
    Given the user is not logged in
    When they use a password manager to autofill credentials
    Then a successful login is expected
    And the user is directed to the home page or dashboard
    And the user is on the Home page
```

```jsx
Feature: User Login
  Scenario: Successful Login with Valid Username and Password
    Given the login page is accessible
    When the user enters a valid username and password
    Then a successful login is expected
    And the user is directed to the home page or dashboard
    And the user is on the Home page
```

```jsx
Feature: User Login
  Scenario: Login with the Forgotten Password
    Given the login page is accessible
    When the user enters an invalid username and password
    Then the Forgotten Password page is expected
    And the user is directed to the Forgotten Password page
    And the user is on the Forgotten Password page
```

```jsx
Feature: User Login
  Scenario: Successful Login with Password Reset Link
    Given the login page is accessible
    When the user uses a valid password reset link to reset the password
    Then a successful login is expected
    And the user is directed to the home page or dashboard
    And the user is on the Home page
```

```jsx
Feature: User Login
  Scenario: Login with Expired Password Reset Link
    Given the user is not logged in
    When they use an expired password reset link
    Then an error message is expected
    And the user receives an error message indicating an expired link
    And the user is still on the login page
```

```jsx
Feature: User Login API

Scenario: API Test for Forgotten Password
  Given the login page is accessible
  When a POST request is sent to /api/login/forgot_password with a valid username, password, and two-factor code
  And there is a user account with a forgotten password
  Then a response containing the forgot password link is received
  And the user is directed to the home page or dashboard
  And the user is on the Login page
```

# Gherkin API Test Cases

## Feature: Login/Registration with Metabase API

```jsx
Background:
Given Metabase API is accessible
```

```jsx
Feature: User Login API

Scenario: API Test for Login with Incorrect Username
  Given the user is not logged in
  When a POST request is sent to /api/login with an incorrect username and a valid password
  And there is a user registered in the system
  Then a response with an error status code and an error message indicating an invalid username is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login with Incorrect Password
  Given the user is not logged in
  When a POST request is sent to /api/login with a valid username and an incorrect password
  And there is a user registered in the system
  Then a response with an error status code and an error message indicating an incorrect password is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login with Empty Fields
  Given the user is not logged in
  When a POST request is sent to /api/login with empty username and password fields
  And there is a user registered in the system
  Then a response with an error status code and an error message indicating that both fields are required is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login with a Locked Account
  Given the user is not logged in
  When a POST request is sent to /api/login with a valid username and password for a locked account
  And there is a user registered in the system with a locked account
  Then a response with an error status code and an error message indicating that the account is locked is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login with a Non-existent Username
  Given the user is not logged in
  When a POST request is sent to /api/login with a username that doesn't exist in the system
  And there is no user registered with that username
  Then a response with an error status code and an error message indicating that the username doesn't exist is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login with an Empty Username
  Given the user is not logged in
  When a POST request is sent to /api/login with an empty username and a valid password
  And there is a user registered in the system
  Then a response with an error status code and an error message indicating an empty username is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login with an Empty Password
  Given the user is not logged in
  When a POST request is sent to /api/login with a valid username and an empty password
  And there is a user registered in the system
  Then a response with an error status code and an error message indicating an empty password is expected
  And the user is still not logged in
```

```jsx
Feature: User Login API

Scenario: API Test for Login Using a Password Manager
  Given the user is not logged in
  When a POST request is sent to /api/login with valid autofilled credentials
  And there is a user registered in the system
  Then a response with a success status code and a message indicating a successful login is expected
  And the user is directed to the home page or dashboard
  And the user is on the Home page
```

```jsx
Feature: User Login API

Scenario: API Test for Successful Login with Valid Username and Password
  Given the login page is accessible
  When a POST request is sent to /api/login with a valid username and password
  And there is a user account that exists
  Then a response with a success status code and a message indicating a successful login is expected
  And the user is directed to the home page or dashboard
  And the user is on the Home page
```

```jsx
Feature: User Login API

Scenario: API Test for Forgotten Password
  Given the login page is accessible
  When a POST request is sent to /api/login/forgot_password with a valid username, password, and two-factor code
  And there is a user account with a forgotten password
  Then a response with a forgot password link is expected
  And the user is directed to the home page or dashboard
  And the user is on the Login page
```

```jsx
Feature: User Login API

Scenario: API Test for Successful Login with Password Reset Link
  Given the login page is accessible
  When a POST request is sent to /api/login with a valid password reset link
  And there is a user account that exists
  Then a response with a success status code and a message indicating a successful login is expected
  And the user is directed to the home page or dashboard
  And the user is on the Home page
```

```jsx
Feature: User Login API

Scenario: API Test for Successful Login with API Token
  Given the login page is accessible
  When a POST request is sent to /api/login with a valid API token
  And there is a user account with an API token
  Then a response with a success status code and a message indicating a successful login is expected
  And the user is directed to the home page or dashboard
  And the user is on the Home page
```

```jsx
Feature: User Login API

Scenario: API Test for Login with Expired Password Reset Link
  Given the user is not logged in
  When a POST request is sent to /api/login with an expired password reset link
  And there is a user account that exists
  Then a response with an error status code and an error message indicating an expired link is expected
  And the user is still not logged in
```

## **Coverage Analysis per Feature (GUI)**

- **Login with Incorrect Username:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with Incorrect Password:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with Empty Fields:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with a Locked Account:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with a Non-existent Username:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with an Empty Username:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with an Empty Password:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login Using a Password Manager:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Successful Login with Valid Username and Password:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Successful Login with Password Reset Link:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Successful Login with API Token:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **Login with Expired Password Reset Link:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
    

## **Coverage Analysis per Feature (GUI)**

- **API Test for Login with Incorrect Username:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with Incorrect Password:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with Empty Fields:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with a Locked Account:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with a Non-existent Username:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with an Empty Username:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with an Empty Password:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login Using a Password Manager:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Successful Login with Valid Username and Password:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Successful Login with Two-Factor Authentication:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Successful Login with Password Reset Link:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Successful Login with API Token:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
- **API Test for Login with Expired Password Reset Link:**
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 100%
    - BVA Coverage: 66.67%
    
    ## **Module Defect Summary**
    
    ### **Measures of Login Page Module (GUI):**
    
    - Number of Decision Tables: 13
    - Number of Boundary Value Analysis (BVA) Test Cases: 12
    - Number of Positive Test Cases: 10
    - Number of Negative Test Cases: 3
    - Number of Passed Test Cases: 6
    - Number of Failed Test Cases: 7
    
    ### **Defect Density for Login Page Module (API):**
    
    - Defect Density: 53.8%
    
    ### **Coverage Analysis for Login Page Module (API):**
    
    - Risk Coverage: 53.8%
    - Decision Table Coverage: 78%
    - BVA Coverage: 66.67%