# Module # 3 Login/Registration

## **Boundary Value Analysis (BVA)** for Login/Registration Validations in Metabase Application:

|  Input Field
   | Minimum  | Minimum +1  |    Average  |    Maximum  | Maximum +1 |
| --- | --- | --- | --- | --- | --- |
| 
  Username
   | 
  7   characters
   | 
  6 characters
   | 
  160 characters
   | 
  319 characters
   | 
 320 characters
   |
| 
  Password
   | 
  13 characters
   | 
  12 characters
   | 
  64 characters
   | 
  127 characters
   | 
 128 characters
   |

## 

| Username Valid (Yes/No) | Username Empty (Yes/No) | Username Incorrect (Yes/No) | Password Valid (Yes/No) | Password Empty (Yes/No) | Password Incorrect (Yes/No) | Account Locked (Yes/No) | Action |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Yes | No | No | Yes | No | No | No | Proceed to Home Page |
| No | Yes | No | No | No | No | No | Display "Username is required” |
| No | No | Yes | Yes | No | No | No | Display "Invalid Username” |
| Yes | No | No | No | No | Yes | No | Display "Invalid Password” |
| No | Yes | No | No | No | No | No | Display "Password is required” |
| No | No | Yes | Yes | No | No | No | Display "Invalid Username” |
| No | No | No | No | No | No | Yes | Display "Account is locked” |

## **Risk Analysis Table** for Login/Registration Validations in Metabase Application:

|         Risk |     Description |    Probability |    Severity |                               Action to Minimize |
| --- | --- | --- | --- | --- |
| 
  Weak Passwords
   | Users choosing weak or easily guessable passwords can lead to security vulnerabilities. | Moderate | High | 1- Password Complexity Requirements: Enforce password complexity requirements, including minimum length, special characters, and a combination of upper and lower case letters. 2- User Education: Educate users on the importance of strong passwords and provide guidance on creating secure passwords. |
| Account Lockout Due to Multiple Failed Attempts | Locking user accounts after multiple failed login attempts can frustrate users and lead to potential denial-of-service attacks. | Low | High | Locking user accounts after multiple failed login attempts can frustrate users and lead to potential denial-of-service attacks. |
| Forgotten Password Recovery | Forgotten Password Recovery | Moderate | Moderate | 1- Password Reset Options: Offer multiple options for password recovery, such as security questions, email verification, or SMS verification. 2- Account Recovery Process: Implement a secure and user-friendly account |
| 
  Credential Theft
   | Unauthorized users gaining access to valid login credentials can result in data breaches and misuse of user accounts. | Low | High | 1- Secure Transmission: Implement secure communication protocols (e.g., HTTPS) to protect login credentials during transmission. 2- Multi-Factor Authentication (MFA): Encourage users to enable MFA for an added layer of security |
| Cookie Management | Poorly managed session cookies can lead to security vulnerabilities and unauthorized access to user accounts. | Moderate | High | 1- Secure Cookie Handling: Implement secure cookie management practices, including secure, http-only, and same-site flags. 2- Session Timeout: Enforce session timeouts to automatically log users out after a period of inactivity. |

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