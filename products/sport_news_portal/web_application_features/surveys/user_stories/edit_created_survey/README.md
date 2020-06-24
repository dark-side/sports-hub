### Back to [Surveys on the portal](/../../) feature

# Allow admin to edit a created survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to edit a created survey

## Acceptance criteria

    Scenario: An admin user edits created survey
    Given I am logged in as an admin user

    When I am on the Surveys page
      And I click on a Not Published survey from the Open list
    Then I see a survey read-only details in reader pool with Delete and Edit buttons
    When I click on an Edit button
    Then I see a edit form with prepopulated data and Cancel, Save buttons
    When I change any information and click Save
    Then I see a updates the survey; saves to database and displays updated in the Open list

## Mockups

1. User sees Published survey in reader pool

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Published survey in reader pool:**

![Published survey in reader pool Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_read_only_not_editable.png)

</details>

## Test Scenarios

1. Verify Editing of Not Published survey
2. Verify Canceling of edited action of Not Published survey

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify Editing of Not Published survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Click on Not Published survey|The system displays survey read-only details in reader pool and Delete and Edit buttons
|6|Click on Edit button|The system displays edit form with prepopulated data and Cancel, Save buttons
|7|Change any information|
|8|Click Save|System updates the survey; saves to database and displays updated in the Open list

### **#2. Verify Canceling of edited action of Not Published survey**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|The system displays filter with options Published/ Not Published
|4|Go to Open list|
|5|Click on Not Published survey|The system displays edit form with prepopulated data and Cancel, Save buttons
|6|Click on Edit button|
|7|Change any information|
|8|Click Cancel|The survey is not edited

</details>
