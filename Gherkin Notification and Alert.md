# Notification & Alert

# **Task 3: Test Cases in Gherkin Language**

**Feature:** Notifications & Alerts

**Background:**

**Given** I am logged in to Metabase

**Scenario 1:** Verify Notification Settings Page

**When** I navigate to the Notification Settings

**Then** the Notification Settings page should be displayed

**Scenario 2**: Create a New Alert

**When** I go to the Alerts section

**And** I click on "New Alert"

**And** I fill in the required information

**And** I save the alert

**Then** the new alert should be created successfully

**Scenario 4:** Delete an Alert

**When** I go to the Alerts section

**And** I select an existing alert

**And** I click on "Delete"

**And** I confirm the deletion

**Then** the alert should be deleted

**Scenario 5:** Test Threshold Values

**When** I create an alert with a low threshold

**And** I ensure the alert triggers

**Then** the alert should trigger when the threshold is met

**Scenario 6:** Test Notification Methods

**When** I create an alert

**And** I set notifications via email and Slack

**And** I trigger the alert

**Then** I should receive notifications through email

**Scenario 8**: Test Integration with Dashboards

**When** I create an alert

**And** I associate it with a specific dashboard

**And** I trigger the alert by changing data on the dashboard

**Then** the alert should trigger when data changes on the associated dashboard

**Scenario 9:** Test Data Security and Privacy

**When** I test the security of notifications data transmission

**Then** the notifications data should be secure and encrypted

**Scenario 10:** Test Performance with Large Data

**When** I create an alert that depends on a large dataset

**And** I monitor performance

**Then** the system should perform well with large datasets

**Scenario 11:** Test Real-Time Updates

**When** I create an alert for real-time data updates

**And** I update the data source

**Then** the alert should trigger in real-time as data updates

**Scenario 12:** Test Third-Party Integration

**When** I create an alert that relies on third-party data sources

**Then** the alert should function correctly with third-party data

**Scenario 14:** Test Data Source Compatibility

**When** I create an alert that integrates with various data sources

**Then** the alert should integrate seamlessly with different data sources

# **Gherkin Test Cases for Web API Testing**

**Feature:** Notifications & Alerts API

**Background:**

**Given** I have a valid API token

**Scenario 1:** Create Alert via API

**When** I send a POST request to create a new alert

**Then** the API should respond with a success status code

**And** the alert is successfully created

**Scenario 2:** Update Alert via API

**When** I send a PUT request to update an existing alert

**Then** the API should respond with a success status code

**And** the alert is successfully updated

**Scenario 3:** Delete Alert via API

**When** I send a DELETE request to delete an alert

**Then** the API should respond with a success status code

**And** the alert is successfully deleted

**Scenario 4:** Retrieve Alert via API

**When** I send a GET request to retrieve alert details

**Then** the API should respond with the alert details

**Scenario 5:** List Alerts via API

**When** I send a GET request to list all alerts

**Then** the API should respond with a list of alerts

**Scenario 6**: Trigger Alert via API

**When** I send a POST request to trigger an alert

**Then** the API should respond with a success status code

**And** the alert is successfully triggered

**Scenario 7**: Test Threshold Values via API

**When** I create an alert via the API with a low threshold

**And** I trigger the alert

**Then** the API should respond with a success status code

**And** the alert triggers when the threshold is met

**Scenario 8:** Test Notification Methods via API

**When** I create an alert via the API with email and Slack notifications

**And** I trigger the alert

**Then** notifications are received through email

**Scenario 9:** Test Alert Scheduling via API

**When** I create a scheduled alert via the API

**And** I wait for the scheduled time

**Then** the API should respond with a success status code

**And** the alert triggers at the scheduled time

**Scenario 10:** Test Integration with Dashboards via API

**When** I create an alert via the API

**And** I associate it with a specific dashboard

**And** I trigger the alert by changing data on the dashboard

**Then** the alert triggers when data changes on the associated dashboard

**Scenario 11**: Test Data Security and Privacy via API

**When** I perform data security testing for API endpoints

**Then** API endpoints should handle data securely and with encryption

**Scenario 12:** Test Performance with Large Data via API

**When** I test the performance of API endpoints with a large dataset

**Then** API endpoints should perform well with large datasets

**Scenario 13:** Test Real-Time Updates via API

**When** I create an alert for real-time data updates via the API

**And I** update the data source

**Then** the alert triggers in real-time as data updates

**Scenario 14:** Test Third-Party Integration via API

**When** I create an alert via the API that relies on third-party data sources

**Then** the API should respond with a success status code

**And** the alert functions correctly with third-party data

**Scenario 15:** Test for Inaccuracy of Data via API

**When** I create an alert for a metric with occasionally inaccurate data via the API

**Then** the API should respond with a success status code

**And** the alert considers data accuracy and triggers accordingly