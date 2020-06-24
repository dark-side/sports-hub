### Back to [Surveys on the portal](../../) feature

# Allow admin to manage surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have Surveys page
    So that I can review and configure surveys

## Acceptance criteria

    Scenario: An admin user visits Surveys page
    Given I am logged in as an admin user

    When I view the application
    Then I see a Surveys menu item in the left sidebar
    When I go to the Surveys page
    Then I see a two tabs Open and Closed, Reader Pool and New Survey button
      And I see the Open tab contains columns:
        - Question
        - Status (Not Published/Published)
        - Actions (for Published - Delete, Close; for Not Published - Publish, Delete)
        - Responses - the number of people who passed the survey
      And I see Unpublished surveys are at the top of the list
      And I see the Closed tab contains columns:
        - Question
        - Close Date
        - Responses - the number of people who passed the survey
        - Delete action per row

## Mockups

1. User sees Open tab on Surveys page
2. User sees Closed tab on Surveys page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees open tab on Surveys page:**

![Open tab on Surveys page Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_open_tab.png)

**2. User sees Closed tab on Surveys page:**

![Closed tab on Surveys page Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_closed_tab.png)

</details>

## Test Scenarios

1. Verify the content of the Surveys page
2. Verify the content of the Open tab on Surveys page
3. Verify the content of the Сlosed tab on Surveys page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of the Surveys page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Observe the content of the Surveys menu item in the left sidebar|The system displays two tabs Open and Closed, Reader Pool and New Survey button

### **#2. Verify the content of the Open tab on Surveys page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Observe the content of the Surveys menu item in the left sidebar|The system displays two tabs Open and Closed, Reader Pool and New Survey button
|5|Click on the Open tab|The Open tab contains columns:<br>- Question<br>- Status (Not Published/Published)<br>- Actions (for Published - Delete, Close; for Not Published - Publish, Delete)<br>- Actions (for Published - Delete, Close; for Not Published - Publish, Delete)<br>- Responses - the number of people who passed the survey

### **#3. Verify the content of the Сlosed tab on Surveys page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Observe the content of the Surveys menu item in the left sidebar|The system displays two tabs Open and Closed, Reader Pool and New Survey button
|5|Click on the Closed tab|The Open tab contains columns:<br>- Question<br>- Close Date<br>- Responses - the number of people who passed the survey<br>- Delete action per row

</details>
