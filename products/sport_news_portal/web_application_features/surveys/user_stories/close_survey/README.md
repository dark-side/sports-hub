### Back to [Surveys on the portal](/../../) feature

# Allow admin to close the survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to close manually or automatically any of surveys

## Acceptance criteria

    Scenario: An admin user closes a survey
    Given I am logged in as an admin user

    When I am on the Surveys page and view Open list
    Then I see a Close action for Published surveys
    When I click to Close
    Then I see a confirmation popup
    When I click to continue
    Then I see a notification about success (failure)
      And I see the survey is moved to Closed list and is not available for users
    When survey end day has passed
    Then I see a moves the survey to Closed list and it’s not available for users

## Mockups

1. User sees Surveys page
2. User sees Close survey option
3. User sees Close survey failure popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Surveys page:**

![Surveys page Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_open_tab.png)

**2. User sees Close survey option:**

![Close survey option](/products/sport_news_portal/web_application_features/surveys/images/close_dropdown_option.png)

**3. User sees Close survey failure popup:**

![Publish survey failure popup](/products/sport_news_portal/web_application_features/surveys/images/failure_popup.png)

</details>

## Test Scenarios

1. Verify that admin can close an existing survey
2. Verify that admin can close a new survey

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can close an existing survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Click on Close for a published survey|
|6|Click on Delete button|The system displays a confirmation popup
|7|Click to continue|The survey is moved to Closed list and is not available for users

### **#2. Verify that admin can close a new survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Click on Add survey button|
|5|Fill in all the needed fields and chose the close date of a survey|
|6|Click Save|The required fields for adding new survey appears
|7|Set up your system time on PC/laptop in order to imitate the time expiration for the survey|The survey is saved and appears in a list
|8|Check if the survey is moved to Closed|The survey should be moved to Closed

</details>
