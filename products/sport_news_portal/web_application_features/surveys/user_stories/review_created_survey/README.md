### Back to [Surveys on the portal](/../../) feature

# Allow admin to review a created survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to review a created survey

## Acceptance criteria

    Scenario: An admin user views a survey with review a created survey
    Given I am logged in as an admin user

    When I am on the Surveys page
    When I click on a Not Published survey from the Open list
    Then I see a survey read-only details in reader pool
      And I see the Delete and Edit buttons
    When I click on a Published survey from the Open or Closed list
    Then I see a survey read-only details in reader pool without any action buttons
      And I see the progress bars for each answer

## Mockups

1. User sees Surveys page
2. User sees Not Published survey in reader pool
3. User sees Published survey in reader pool

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees open tab on Surveys page:**

![Open tab on Surveys page Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_open_tab.png)

**2. User sees Not Published survey in reader pool:**

![Not Published survey in reader pool](/products/sport_news_portal/web_application_features/surveys/images/surveys_read_only_editable.png)

**3. User sees Published survey in reader pool:**

![Published survey in reader pool Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_read_only_not_editable.png)

</details>

## Test Scenarios

1. Verify clicking on Published survey
2. Verify clicking on Not Published survey

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify clicking on Published survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Click on Published survey|The system displays survey read-only details in reader pool and progress bars for each answer

### **#2. Verify clicking on Not Published survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Click on Not Published survey|The system displays survey read-only details in reader pool and Delete and Edit buttons

</details>
