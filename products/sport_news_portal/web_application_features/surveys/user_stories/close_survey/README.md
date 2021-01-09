### Back to [Surveys on the portal](../../) feature

# Allow admin to close the survey

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to close the surveys

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user closes a survey</i></b>

Given I am logged in as an admin user

When I am on the <b>Surveys</b> page and view the <b>Open</b> tab
Then I see the <b>Close</b> action for surveys in <b>Published</b> state

When I click <b>Close</b>
Then I see a success message
  And I see the survey is moved to the <b>Closed</b> tab and is not available for users

When the survey configured end day has passed
Then I see the survey is automaticaly moved to <b>Closed</b> tab and is not available for users

When I go to the <b>Closed</b> tab
Then I see a list of closed surveys that contain:
  - Question
  - Closed date
  - Responses – the number of people who passed the survey
  - Delete icon for each row

When I click on any survey on the <b>Closed</b> tab
Then I see survey read-only details in <b>Reader pool</b> on the right side without any action buttons
  And I see the progress bars for each answer

When I hover over the survey in the list
Then I see a <b>Delete</b> icon

When I click on the <b>Delete</b> icon
Then I see a confirmation dialog

When I confirm delete on the confirmation dialog
Then I see a success message
  And I see the survey is removed from the list
</pre>

## Mockups

1. Admin user sees actions for published survey
2. Admin user sees a Closed tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for published survey:**

![Admin user sees actions for published survey](/products/sport_news_portal/web_application_features/surveys/images/admin_published_actions.png)

**2. Admin user sees a Closed tab:**

![Admin user sees a Closed tab](/products/sport_news_portal/web_application_features/surveys/images/admin_surveys_closed_tab.png)

</details>

## Test cases

1. Verify that admin can close a published survey
2. Verify that survey is closed automatically when the end day of range is passed
3. Verify the content of the Closed tab on the Surveys page
4. Verify that it is possible to delete the Closed survey

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can close a published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey|1) Click published survey/br>2) Click the <b>Publish</b> state/br>3) Select <b>Close</b> action|3) Survey moved to the <b>Closed tab<b>. The survey is not available for users to vote|

### **#2. Verify that survey is closed automatically when the end day of range is passed**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey with a configured end date (mm.dd.yyyy)|1) Check when the selected date passed|1) Survey moved to the <b>Closed tab</b>. The survey is not available for users to vote|

### **#3. Verify the content of the Closed tab on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Observe the content of the <b>Closed</b> tab|1) There is a table with 3 columns:</br>- Question (text of question)</br>- Closed date</br>- Responses (amount of users who responded to the survey). When the user hovers over a row, the Delete icon appears|

### **#4. Verify that it is possible to delete the Closed survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a closed survey|1) Click closed survey</br>2) Click <b>Delete</b></br>3) Confirm on the confirmation dialog|2) The survey is removed from the <b>Closed</b> tab|

</details>
