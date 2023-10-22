# Database Connection

# Gherkin GUI Test Cases

## Feature: Database Connectivity in Metabase

```jsx
Background:
Given Metabase application is open
```

```jsx
Scenario: Verify Successful Connection
When I enter valid database credentials
And I provide a valid host address
Then I attempt to connect to the database
And I should see "Successful connection" as the result
```

```jsx
Scenario: Verify Connection Failure - Invalid Credentials
When I enter invalid database username and password
And I provide a valid host address
Then I attempt to connect to the database
And I should see a connection failure message
```

```jsx
Scenario: Verify Username Required Field Validation
When I leave the username field empty
And I provide a valid password
Then I attempt to connect to the database
And I should see "Username required" as the error message
```

```jsx
Scenario: Verify Password Required Field Validation
When I provide a valid username
And I leave the password field empty
Then I attempt to connect to the database
And I should see "Password required" as the error message
```

```jsx
Scenario: Verify Invalid Host Address
When I enter an invalid host address
And I provide valid credentials
Then I attempt to connect to the database
And I should see a connection failure message due to an invalid host
```

```jsx
Scenario: Verify Maximum Username Length
When I enter a 255-character username
And I provide a valid password
Then I attempt to connect to the database
And I should see a successful connection with a maximum length username
```

```jsx
Scenario: Verify Minimum Password Length
When I enter a 1-character password
And I provide a valid username
Then I attempt to connect to the database
And I should see a successful connection with a minimum length password
```

```jsx
Scenario: Verify Maximum Password Length
When I enter a 128-character password
And I provide a valid username
Then I attempt to connect to the database
And I should see a successful connection with a maximum length password
```

```jsx
Scenario: Verify Invalid Username Length (Less than Minimum)
When I leave the username field empty
And I provide a valid password
Then I attempt to connect to the database
And I should see "Invalid username" as the error message
```

```jsx
Scenario: Verify Invalid Username Length (More than Maximum)
When I enter a 256-character username
And I provide a valid password
Then I attempt to connect to the database
And I should see "Invalid username" as the error message
```

```jsx
Scenario: Verify Invalid Password Length (Less than Minimum)
When I provide a valid username
And I leave the password field empty
Then I attempt to connect to the database
And I should see "Invalid password" as the error message
```

```jsx
Scenario: Verify Invalid Password Length (More than Maximum)
When I provide a valid username
And I enter a 129-character password
Then I attempt to connect to the database
And I should see "Invalid password" as the error message
```

```jsx
Scenario: Verify Successful Connection with Valid Host Address
When I enter valid database credentials
And I provide a valid host address
Then I attempt to connect to the database
And I should see a successful connection to the database
```

```jsx
Scenario: Verify Connection Failure with Invalid Host Address
When I enter valid database credentials
And I enter an invalid host address
Then I attempt to connect to the database
And I should see a connection failure message due to an invalid host
```

```jsx
Scenario: Verify Behavior with Valid Credentials and Timeout
When I enter valid database credentials
And I set a long connection timeout
Then I attempt to connect to the database
And I should either see a successful connection or a timeout message
```

# Gherkin API Test Cases

## Feature: Database Connectivity with Metabase API

```jsx
Background:
Given Metabase API is accessible
```

```jsx
Scenario: Verify Database Connection Status
When I send a GET request to "/api/database/status"
Then the response should indicate the status of the database connection
```

```jsx
Scenario: Verify List of Databases
When I send a GET request to "/api/database"
Then the response should contain a list of available databases
```

```jsx
Scenario: Verify Database Schema Information
When I send a GET request to "/api/database/{database_id}/schema"
Then the response should include schema information for the specified database
```

```jsx
Scenario: Verify Query Execution
When I send a POST request to "/api/database/{database_id}/query" with a valid SQL query
Then the response should include the query result, and the status should be "success"
```

```jsx
Scenario: Verify Query Execution - Invalid SQL
When I send a POST request to "/api/database/{database_id}/query" with an invalid SQL query
Then the response should indicate a query error, and the status should be "failed"
```

```jsx
Scenario: Verify Query Execution - No Permission
When I send a POST request to "/api/database/{database_id}/query" with a query that the user has no permission to execute
Then the response should indicate a permission error
```

```jsx
Scenario: Verify Query Execution - Timeout
When I send a POST request to "/api/database/{database_id}/query" with a long-running query
Then the response should indicate a timeout error
```

```jsx
Scenario: Verify Query Cancellation
When I send a POST request to "/api/database/{database_id}/query/{query_id}/cancel" to cancel a running query
Then the response should confirm that the query has been canceled
```

```jsx
Scenario: Verify Query Result Export - CSV
When I send a GET request to "/api/database/{database_id}/query/{query_id}/results.csv" to export query results in CSV format
Then the response should provide a downloadable CSV file
```

```jsx
Scenario: Verify Query Result Export - JSON
When I send a GET request to "/api/database/{database_id}/query/{query_id}/results.json" to export query results in JSON format
Then the response should provide query results in JSON format
```

```jsx
Scenario: Verify Query Result Export - XLSX
When I send a GET request to "/api/database/{database_id}/query/{query_id}/results.xlsx" to export query results in XLSX format
Then the response should provide a downloadable XLSX file
```

```jsx
Scenario: Verify Query History Retrieval
When I send a GET request to "/api/database/{database_id}/query/{query_id}/history" to retrieve query history
Then the response should contain the history of the specified query
```

```jsx
Scenario: Verify Database Disconnect
When I send a POST request to "/api/database/{database_id}/disconnect" to disconnect from the database
Then the response should confirm the disconnection
```

```jsx
Scenario: Verify Connection Pool Information
When I send a GET request to "/api/database/{database_id}/pool" to retrieve connection pool information
Then the response should include details about the connection pool
```

```jsx
Scenario: Verify Database Backup
When I send a POST request to "/api/database/{database_id}/backup" to initiate a database backup
Then the response should indicate the status of the backup process
```