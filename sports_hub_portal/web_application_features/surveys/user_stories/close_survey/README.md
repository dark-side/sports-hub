### Back to [Surveys on the portal](../../README.md) feature

# Allow admin to close surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to close surveys

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user closes a survey</i></b>

Given I am logged in as an admin user

When I am on the <b>Surveys</b> page and view the <b>Opened</b> tab
Then I see the <b>Close</b> action for surveys in <b>Published</b> status

When I click <b>Close</b>
Then I see a success message
  And I see the survey is moved to the <b>Closed</b> tab and is not available for users

When the survey configured end day has passed
Then I see the survey is automatically moved to the <b>Closed</b> tab and is not available for users

When I go to the <b>Closed</b> tab
Then I see a list of closed surveys that contain:
  - Question
  - Closed date
  - Responses – the number of people who passed the survey
  - Delete icon for each row

When I select any survey on the <b>Closed</b> tab
Then I see survey read-only details in <b>Reader Poll</b> on the right side without any action buttons
  And I see the progress bars for each answer

When I hover over the survey on the list
Then I see the delete icon

When I click the delete icon
Then I see a confirmation dialog

When I confirm deletion on the confirmation dialog
Then I see a success message
  And I see the survey is removed from the list
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions for the published survey
2. Admin user sees the <b>Closed</b> tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the published survey:**

![Admin user sees actions for the published survey](/sports_hub_portal/web_application_features/surveys/images/admin_published_actions.png)

**2. Admin user sees the Closed tab:**

![Admin user sees the Closed tab](/sports_hub_portal/web_application_features/surveys/images/admin_surveys_closed_tab.png)

</details>

## Test cases

1. Verify that admin can close the published survey
2. Verify that survey is closed automatically when the end day of range is passed
3. Verify the content of the <b>Closed</b> tab on the <b>Surveys</b> page
4. Verify that it is possible to delete the closed survey

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can close the published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey|1) Select the published survey</br>2) Click the <b>Published</b> status</br>3) Select <b>Close</b> action|3) The survey is moved to the <b>Closed</b> tab. The survey is not available for users to vote|

### **#2. Verify that survey is closed automatically when the end day of range is passed**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is the published survey with a configured end date (mm.dd.yyyy)|1) Check when the selected date passes|1) The survey is moved to the <b>Closed</b> tab. The survey is not available for users to vote|

### **#3. Verify the content of the Closed tab on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Observe the content of the <b>Closed</b> tab|1) There is a table with 3 columns:</br>- Question (text of question)</br>- Closed date</br>- Responses (amount of users who responded to the survey). When the user hovers over a row, the delete icon appears|

### **#4. Verify that it is possible to delete the closed survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a closed survey|1) Select the closed survey</br>2) Click <b>Delete</b></br>3) Confirm on the confirmation dialog|2) The survey is removed from the <b>Closed</b> tab|

</details>
