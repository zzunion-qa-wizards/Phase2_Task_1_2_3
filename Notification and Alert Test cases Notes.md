# Notification & Alert

**Gui Test_Cases**

| Test Case
  ID | Test Case | Test Steps | Expected Result | Actual Result | Pre-Condition | Post-Condition | Test Data |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC_GUI_01 | Verify Notification Settings
  Page | 1. Log in to Metabase. 2.
  Navigate to Notification Settings | Notification Settings page is
  displayed. | Notification Settings page is
  displayed. | User is logged in to Metabase. | User is on the Notification Settings page. | Null |
| TC_GUI_02 | Create a New Alert | 1. Log in to Metabase. 2. Go to
  the Alerts section. 3. Click on "New Alert". 4. Fill in the
  required information. 5. Save the alert. | The new alert is created
  successfully. | The new alert is created
  successfully | User is logged in to Metabase.
  Alerts section is accessible. | A new alert is created and saved. | Alert details data. |
| TC_GUI_03 | Edit an Existing Alert | 1. Log in to Metabase. 2. Go to
  the Alerts section. 3. Select an existing alert. 4. Click on
  "Edit". 5. Modify the alert details. 6. Save the changes. | The alert details are updated. | The alert details are
  updated.  | User is logged in to Metabase.
  Existing alert is selected.  | Alert details are updated and
  saved. | Alert details data. |
| TC_GUI_04 | Delete an Alert | 1. Log in to Metabase. 2. Go to
  the Alerts section. 3. Select an existing alert. 4. Click on
  "Delete". 5. Confirm the deletion. | The alert is deleted | The alert is deleted. | User is logged in to Metabase.
  Existing alert is selected | Alert is deleted. | Alert details data. |
| TC_GUI_05 | Test Threshold Values | 1. Log in to Metabase. 2. Create
  an alert with a low threshold. 3. Ensure the alert triggers. | The alert triggers when the
  threshold is met. | The alert triggers when the
  threshold is met. | User is logged in to Metabase. | Alert with a low threshold is created. | Alert details and data. |
| TC_GUI_06 | Test Notification Methods | 1. Log in to Metabase. 2. Create
  an alert. 3. Set notifications via email and Slack. 4. Trigger the alert. | Receive notifications through
  email and Slack. |  Receive notifications through email and
  Slack. | User is logged in to Metabase. | Alert with email and Slack
  notifications is created. | Alert details and data. |
| TC_GUI_07 | Test Alert Scheduling | 1. Log in to Metabase. 2. Create
  a recurring alert. 3. Schedule it for a specific time. 4. Wait for the
  scheduled time. | The alert triggers at the
  scheduled time. |  The alert triggers at the scheduled time. | User is logged in to Metabase. | Recurring alert is scheduled | Alert details and data. |
| TC_GUI_08 | Test Integration with Dashboards | 1. Log in to Metabase. 2. Create
  an alert. 3. Associate it with a specific dashboard. 4. Trigger the alert by
  changing data on the dashboard. | The alert triggers when data
  changes on the associated dashboard. | The alert triggers when data
  changes on the associated dashboard.  | User is logged in to Metabase. | Alert is associated with a
  specific dashboard. | Alert details and data. |
| TC_GUI_09 | Test Data Security and Privacy | 1. Log in to Metabase. 2. Test
  the security of notifications data transmission. | Notifications data is secure and
  encrypted. | Notifications data is secure and
  encrypted. | User is logged in to Metabase. | Security testing environment is
  set up. | Test data for data security. |
| TC_GUI_10 | Test Performance with Large Data | 1. Log in to Metabase. 2. Create
  an alert that depends on a large dataset. 3. Monitor performance. | The system performs well with
  large datasets. | The system performs well with
  large datasets.  | User is logged in to Metabase.
  Large dataset is available | Alert is created and tested with
  large dataset. | Large dataset and alert details
  data. |
| TC_GUI_11 | Test Real-Time Updates | 1. Log in to Metabase. 2. Create
  an alert for real-time data updates. 3. Update the data source. | The alert triggers in real-time
  as data updates. | The alert triggers in real-time
  as data updates. | User is logged in to Metabase. | Real-time data updates environment
  is set up. | Data source updates and alert
  details data. |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
| TC_GUI_12 | Test Data Source Compatibility | 1. Log in to Metabase. 2. Create
  an alert that integrates with various data sources. | The alert integrates seamlessly
  with different data sources. | The alert integrates seamlessly
  with different data sources. | Alert is created and tested with
  various data sources. | Alert details and data source
  information. | lert details and data source
  information |
| TC_GUI_13 | Test Delayed Data Updates | 1. Log in to Metabase. 2. Create
  an alert for delayed data updates. 3. Simulate a delay. | The alert triggers after a data
  update delay. | The alert triggers after a data
  update delay. | Delayed data updates simulation
  and alert details data. | Nothing | null |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |

# Test_Cases for Web Api

| Test Case
  ID | Test Case | Description | HTTP Method | Expected Result | Actual Result | Pre-Condition | Post-Condition |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TC_001 | Create Alert via API | Create a new alert via the API. | POST | The alert is successfully
  created. | Pending | Valid API token is available. | A new alert is created in the
  system. |
| TC_002 | Update Alert via API | Update an existing alert via the
  API. | PUT | The alert is successfully
  updated. | Pending | Valid API token is available.
  Existing alert exist | Alert details data for the updated
  alert. |
| TC_003 | Delete Alert via API | Delete an alert via the API. | DELETE | The alert is successfully
  deleted. | Pending | Valid API token is available.
  Existing alert exists. | Alert is deleted from the system. |
| TC_004 | Retrieve Alert via API | Retrieve alert details via the
  API. | GET | The alert details are returned. | Pending | Valid API token is available. | Alert details are fetched from the
  system |
| TC_005 | List Alerts via API | List all alerts via the API. | GET | A list of alerts is returned. | Pending | Valid API token is available | A list of alerts is fetched from
  the system. |
| TC_006 | Trigger Alert via API | Trigger an alert via the API. | POST | The alert is successfully
  triggered. | Pending | Valid API token is available.
  Alert exists. | Alert is triggered |
| TC_007 | Test Threshold Values via API | Create an alert with a low
  threshold via the API and trigger it. | POST | The alert triggers when the
  threshold is met. | Pending | Valid API token is available. | Alert with a low threshold is
  created. |
| TC_008 | Test Notification Methods via API | Create an alert via the API with
  email and Slack notifications. Trigger the alert. | POST | Receive notifications through
  email and Slack. | Pending | Valid API token is available. | Alert with email and Slack
  notifications is created. |
| TC_009 | Test Alert Scheduling via API | Create a scheduled alert via the
  API and wait for the scheduled time. | POST | The alert triggers at the
  scheduled time. | Pending | Valid API token is available. | Recurring alert is schedule |
| TC_010 | Test Integration with Dashboards
  via API | Create an alert via the API and
  associate it with a specific dashboard. Trigger the alert by changing data on
  the dashboard. | POST | The alert triggers when data
  changes on the associated dashboard. | Pending | Valid API token is available.
  Dashboard is associate | Alert is associated with the dashboard. |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
| TC_011 | Test Real-Time Updates via API | Create an alert for real-time
  data updates via the API and update the data source. | POST | The alert triggers in real-time
  as data updates. | Pending | Valid API token is available.
  Real-time data updates are enabled. | Real-time data updates are
  simulated, and the alert triggers. |
| TC_012 | Test Third-Party Integration via
  API | Create an alert via the API that
  relies on third-party data sources. | POST | The alert functions correctly
  with third-party data. | Pending | Valid API token is available.
  Third-party data sources are integrated | Alert functions correctly with
  third-party data. |
|  |  |  |  |  |  |  |  |