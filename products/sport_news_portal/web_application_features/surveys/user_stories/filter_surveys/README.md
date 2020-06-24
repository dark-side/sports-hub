### Back to [Surveys on the portal](../../) feature

# Allow admin to filter surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to filter opened surveys

## Acceptance criteria

    Scenario: An admin user filters surveys
    Given I am logged in as an admin user

    When I am on the Surveys page and view Open list
    Then I see a filter with options Published/ Not Published
    When I select Published
    Then I see only Published surveys and their amount
    When I select Not Published
    Then I see only Not Published surveys and their amount

## Mockups

1. User sees Surveys page
2. User sees Filter surveys options

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Surveys page:**

![Surveys page Screen](/products/sport_news_portal/web_application_features/surveys/images/surveys_open_tab.png)

**1. User sees Filter surveys options:**

![Filter surveys options Screen](/products/sport_news_portal/web_application_features/surveys/images/filter_options.png)

</details>

## Test Scenarios

1. Verify ability to filter Published surveys
2. Verify ability to filter Not Published surveys

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify ability to filter Published surveys**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Go to Open list|
|5|Click on Surveys filter icon|The system displays filter with options Published/ Not Published
|6|Select Published|The system displays only Published surveys and their amount

### **#2. Verify ability to filter Not Published surveys**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on the Surveys menu item in the left sidebar|
|4|Go to Open list|
|5|Click on Surveys filter icon|The system displays filter with options Published/ Not Published
|6|Select Not Published|The system displays only Not Published surveys and their amount

</details>
