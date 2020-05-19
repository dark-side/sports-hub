### Back to [Surveys on the portal](/../../) feature

# Allow admin to delete a survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to publish the surveys
    So that the users can vote

## Acceptance criteria

    Scenario: An admin user publishes the survey
    Given I am logged in as an admin user

    When I am on the Surveys page and view Open list
      And I select Not Published survey and click Publish
    Then I see a confirmation popup
    When I click to continue
    Then I see a notification about success (failure)
      And I see the survey in the users’ personal cabinet

## Mockups

1. User sees Surveys page
2. User sees Publish survey confirmation popup
3. User sees Survey is published popup
4. User sees Publish survey failure popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Surveys page:**

![Surveys page Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_open_tab.png)

**2. User sees Publish survey confirmation popup:**

![Publish survey confirmation popup](/products/sport_news_portal/web_application_features/surveys/images/publish_conformation.png)

**3. User sees Survey is published popup:**

![Survey is published popup](/products/sport_news_portal/web_application_features/surveys/images/published_notification_popup.png)

**4. User sees Publish survey failure popup:**

![Publish survey failure popup](/products/sport_news_portal/web_application_features/surveys/images/failure_popup.png)

</details>

## Test Scenarios

1. Verify deleting of the survey

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can publish a survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Select Not Published Survey|
|6|Click Publish|The system displays a confirmation popup
|7|Click to continue|The system displays a notification about success (failure) and the survey is displayed in the user's personal cabinet

</details>
