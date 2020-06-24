### Back to [Surveys on the portal](../../) feature

# Allow admin to delete a survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to delete any of surveys

## Acceptance criteria

    Scenario: An admin user deletes a survey
    Given I am logged in as an admin user

    When I am on the Surveys page and view Open or Closed list
      And I select any of the surveys and click Delete button
    Then I see a confirmation popup
    When I click to continue
    Then I see a notification about success (failure)
      And I see the survey is removed (not removed) from the list

## Mockups

1. User sees Delete survey icon
2. User sees Delete survey confirmation popup
3. User sees Delete survey failure popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Delete survey icon:**

![Delete survey icon Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_with_delete_icon.png)

**2. User sees Delete survey confirmation popup:**

![Delete survey confirmation popup](/products/sport_news_portal/web_application_features/surveys/images/delete_confirmation_popup.png)

**3. User sees Delete survey failure popup:**

![Delete survey failure popup](/products/sport_news_portal/web_application_features/surveys/images/failure_popup.png)

</details>

## Test Scenarios

1. Verify deleting of the survey

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify deleting of the survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Click on any survey|The system displays survey read-only details in reader pool and Delete and Edit buttons
|6|Click on Delete button|The system displays a confirmation popup
|7|Click Continue on a confirmation popup|The system displays a notification about success and the survey is removed from the list

</details>
