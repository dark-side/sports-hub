### Back to [Surveys on the portal](../../) feature

# Allow users to see My Surveys page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to have My Surveys page
    So that I can vote

## Acceptance criteria

    Scenario: A site user visits My Surveys page
    Given I am logged in as a site user

    When I click on a dropdown menu next to my avatar at the top of the page
    Then I see the My Surveys menu item
    When I click to My Surveys
    Then I am in a personal cabinet and My Survey tab are actived
      And I see the system displays only Published by admin surveys here
      And I see the system displays two tabs Open and Closed
      And I see the Open and a first survey are actived
      And I see the Open list is sorted by creation date and contains columns:
        - Question
        - Due Date
      And I see the Closed list contains surveys that I participated in and columns:
        - Question
        - Close Date

## Mockups

1. User sees My Surveys page -> Open tab
2. User sees My Surveys page -> Closed tab

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees My Surveys page -> Open tab:**

![My Surveys page -> Open tab](/products/sport_news_portal/web_application_features/surveys/images/my_surveys_opened.png)

**2. User sees My Surveys page -> Closed tab:**

![My Surveys page -> Closed tab Screen](/products/sport_news_portal/web_application_features/surveys/images/my_surveys_closed.png)

</details>

## Test Scenarios

1. Verify that My Survey tab in a personal cabinet
2. Verify the content of Open tab on My Survey tab
3. Verify the content of Closed tab on My Survey tab

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that My Survey tab in a personal cabinet**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a dropdown menu next to my avatar at the top of the page|The system displays My Surveys menu item
|4|Click to My Surveys|Then the system takes me to a personal cabinet and My Survey tab is active

### **#2. Verify the content of Open tab on My Survey tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a dropdown menu next to my avatar at the top of the page|The system displays My Surveys menu item
|4|Click to My Surveys|Then the system takes me to a personal cabinet and My Survey tab is active
|5|Go to Open tab|Open list is sorted by creation date and contains columns:<br>- Question<br>- Due Date

### **#3. Verify the content of Closed tab on My Survey tab**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a dropdown menu next to my avatar at the top of the page|The system displays My Surveys menu item
|4|Click to My Surveys|Then the system takes me to a personal cabinet and My Survey tab is active
|5|Go to Closed tab|Closed list contains surveys that I participated in and columns:<br>- Question<br>- Close Date

</details>
