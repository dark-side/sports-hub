### Back to [Surveys on the portal](/../../) feature

# Allow admin to create a survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to create a survey

## Acceptance criteria

    Scenario: An admin user creates a survey
    Given I am logged in as an admin user

    When I am on the Surveys page and click on New Survey button
    Then I see a form in reader pool
      And I see the form contains:
        - a field for a question - required
        - a calendar to select a period - required and cannot be in the past
        - a field for answer options - required
        - a link to add one more answer
        - Cancel and Save buttons
    When I fill in question and answer options and click Save
    Then I see a saves the survey to the database in Not Published status
      And I see a survey question appears in the Open list

## Mockups

1. User sees Create new survey form
2. User sees survey calendar

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Create new survey form:**

![Create new survey Screen](/products/sport_news_portal/web_application_features/surveys/images/edit_mode.png)

**2. User sees survey calendar:**

![Survey calendar Screen](/products/sport_news_portal/web_application_features/surveys/images/survey_calendar.png)

</details>

## Test Scenarios

1. Verify clicking on New Survey button of the Surveys page
2. Verify the content the form in the reader pool on the Surveys page
3. Verify that survey are saved to the database in Not Published status

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify clicking on New Survey button of the Surveys page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Observe the content of the Surveys menu item in the left sidebar|The system displays two tabs Open and Closed, Reader Pool and New Survey button
|5|Click on New Survey button|The system displays a form in reader pool

### **#2. Verify the content the form in the reader pool on the Surveys page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Observe the content of the Surveys menu item in the left sidebar|The system displays two tabs Open and Closed, Reader Pool and New Survey button
|5|Click on New Survey button|
|6|Observe the content of the form in reader pool|The system displays a form in reader pool that contains:<br>- a field for a question - required<br>- a calendar to select a period - required and cannot be in the past<br>- a field for answer options - required<br>- a link to add one more answer<br>- Cancel and Save buttons

### **#3. Verify that survey are saved to the database in Not Published status**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Observe the content of the Surveys menu item in the left sidebar|The system displays two tabs Open and Closed, Reader Pool and New Survey button
|5|Click on New Survey button|
|6|Fill in question and answer options|
|7|Click Save button|The system saves the survey to the database in Not Published status and a survey question appears in the Open list

</details>
