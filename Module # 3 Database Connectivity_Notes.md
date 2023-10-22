# Module # 3 Database Connectivity

## Equivalence Class Partitioning (ECP) for Database Connectivity in Metabase Application:

| Test Case ID | Description | Input Data | Expected Output |
| --- | --- | --- | --- |
| TC_ECP_01 | Valid database credentials | Valid username, password | Successful connection |
| TC_ECP_02 | Invalid database credentials | Invalid username, password | Connection failure message |
| TC_ECP_03 | Empty username field | Empty string, password | Error: Username required |
| TC_ECP_04 | Empty password field | Valid username, empty string | Error: Password required |
| TC_ECP_05 | Invalid database host | Invalid host address | Connection failure message |

## Boundary Value Analysis (BVA) for Database Connectivity in Metabase Application:

| Test Case ID | Description | Input Data | Expected Output |
| --- | --- | --- | --- |
| TC_BVA_01 | Minimum valid username length | 1-character username | Successful connection |
| TC_BVA_02 | Maximum valid username length | 255-character username | Successful connection |
| TC_BVA_03 | Minimum valid password length | 1-character password | Successful connection |
| TC_BVA_04 | Maximum valid password length | 128-character password | Successful connection |
| TC_BVA_05 | Invalid username length (less than minimum) | 0-character username | Error: Invalid username |
| TC_BVA_06 | Invalid username length (more than maximum) | 256-character username | Error: Invalid username |
| TC_BVA_07 | Invalid password length (less than minimum) | 0-character password | Error: Invalid password |
| TC_BVA_08 | Invalid password length (more than maximum) | 129-character password | Error: Invalid password |
| TC_BVA_09 | Valid host address length | Valid host address | Successful connection |
| TC_BVA_10 | Invalid host address format | Invalid host address | Error: Invalid host |

## Risk Analysis Matrices for Database Connectivity in Metabase Application:

| Test Case ID | Description | Risk Level | Input Data | Expected Output |
| --- | --- | --- | --- | --- |
| TC_RA_01 | Valid database credentials | Low | Valid username, password | Successful connection |
| TC_RA_02 | Invalid database credentials | High | Invalid username, password | Connection failure message |
| TC_RA_03 | Empty username field | Medium | Empty string, password | Error: Username required |
| TC_RA_04 | Empty password field | Medium | Valid username, empty string | Error: Password required |
| TC_RA_05 | Invalid database host | High | Invalid host address | Connection failure message |