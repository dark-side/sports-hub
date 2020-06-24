### Back to [Surveys on the portal](/../../) feature

# Allow users to see form for voting

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to have a voting form
    So that I can submit my answer

## Acceptance criteria

    Scenario: A site user submits a survey
    Given I am logged in as a site user

    When I am on My Surveys page
    When I click on any of Open survey
    Then I see a form in reader pool
      And I see the form contains a question, answer options, active "Next" question and non-active "See the results" buttons
    When I click on Next
    Then I see the next survey
    When I choose an answer
    Then I see my answer is immediately saved
    When I click on Next
    Then I see the survey is Closed and displays the next survey
    When I choose an answer
    Then I see the results button is active
    When I click on See the results
    Then I see a progress bars of the answers
      And I see the Next button is active and "See the results" becomes inactive

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

1. Verify the content of a reader pool form for user
2. Verify clicking on See the results in a reader pool form for user

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of a reader pool form for user**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a dropdown menu next to my avatar at the top of the page|The system displays My Surveys menu item
|4|Click to My Surveys|Then the system takes me to a personal cabinet and My Survey tab is active
|5|Go to open tab|
|6|Click on any open survey|
|7|Observe the content of a reader pool form for user|A form contains a question, answer options, active "Next" question and non-active "See the results" buttons

### **#2. Verify clicking on See the results in a reader pool form for user**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a dropdown menu next to my avatar at the top of the page|The system displays My Surveys menu item
|4|Click to My Surveys|Then the system takes me to a personal cabinet and My Survey tab is active
|5|Go to open tab|
|6|Click on any open survey|The reader pool form for user is opened
|7|Click on Next button|The system moves the survey to Closed and displays the next survey
|8|Choose an answer|The results button is active
|9|Click on See the results|Then the system displays progress bars of the answers and the "Next" button is active and "See the results" becomes inactive

</details>
