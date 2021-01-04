### Back to [Surveys on the portal](../../) feature

# Allow admin to create surveys on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to create surveys on the portal

## Acceptance criteria

<pre>
Scenario: An admin user configures surveys on the portal
Given I am logged in as an admin user

When I view the site
Then I see the Surveys menu item on the left sidebar menu

When I go to the <b>Surveys</b> configuration page
Then I see <b>Open</b> and <b>Closed</b> tabs, the <b>Reader pool</b> section, and <b>+ New Survey</b> button
  And I see the <b>Open</b> tab contains:
    - Question
    - Status (Not published, Published)
    - Actions (for Published: Close; for Not published: Publish)
    - Responses – the number of people who passed the survey
    - Delete icon for each row
  And I see unpublished surveys are at the top of the list

When I click <b>+ New Survey</b>
Then I see a new survey form on the right side that contains
  - A text field for a question, required field
  - A calendar icon to select a period for voting, required and cannot be selected for the past date
  - Input field for answer option, required field
  - Link button to add one more answer option
  - <b>Cancel</b> and <b>Save</b> buttons

When I enter a new question with options and click <b>Save</b>
Then I see the survey is saved to the database in the <b>Not published</b> state
  And I see a survey question appears at the top of the list on the <b>Open</b> tab

When I click on the <b>Not published</b> survey on the <b>Open</b> tab
Then I see the survey read-only details in the <b>Reader pool</b> on the right side
  And I see the <b>Delete</b> and <b>Edit</b> buttons

When I click <b>Edit</b>
Then I see edit form with pre-populated data, the <b>Cancel</b> and <b>Save</b> buttons

When I change any information and click <b>Save</b>
Then I see the updated survey on the <b>Open</b> tab

When I click on the <b>Not published</b> survey and <b>Delete</b> button in the <b>Reader pool</b>
Then I see a confirmation dialog

When I confirm delete on the confirmation dialog
Then I see a success message
  And I see the survey is removed from the list

When I hover over the survey in the list
Then I see a <b>Delete</b> icon

When I click on the <b>Delete</b> icon
Then I see a confirmation dialog

When I confirm delete on the confirmation dialog
Then I see a success message
  And I see the survey is removed from the list
</pre>

## Mockups

1. Admin user sees an Open tab and published survey in the Reader pool
2. Admin user clicked New Survey and sees a new survey form
3. Admin user sees a calendar to select survey period
4. Admin user sees a non-published survey in the Reader pool
5. Admin user edits a non-published survey in the Reader pool
6. Admin user sees a delete confirmation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees an Open tab and published survey in the Reader pool:**

![Admin user sees an Open tab and published survey in the Reader pool](/products/sport_news_portal/web_application_features/surveys/images/admin_surveys_open_tab.png)

**2. Admin user clicked New Survey and sees a new survey form:**

![Admin user clicked New Survey and sees a new survey form](/products/sport_news_portal/web_application_features/surveys/images/admin_new_survey_form.png)

**3. Admin user sees a calendar to select survey period:**

![Admin user sees a calendar to select survey period](/products/sport_news_portal/web_application_features/surveys/images/admin_new_survey_calendar.png)

**4. Admin user sees a non-published survey in the Reader pool:**

![Admin user sees a non-published survey in the Reader pool](/products/sport_news_portal/web_application_features/surveys/images/admin_non_published_survey.png)

**5. Admin user edits a non-published survey in the Reader pool:**

![Admin user edits a non-published survey in the Reader pool](/products/sport_news_portal/web_application_features/surveys/images/admin_edit_non_published_survey.png)

**6. Admin user sees a delete confirmation popup:**

![Admin user sees a delete confirmation popup](/products/sport_news_portal/web_application_features/surveys/images/admin_delete_confirmation.png)

</details>

## Test cases

1. Verify the tabs on the Surveys page
2. Verify the content of the Open tab on the Surveys page
3. Verify the content of the new Survey form on a Surveys page
4. Verify that it is not possible to save survey without question
5. Verify that it is not possible to select the past dates for the survey
6. Verify that it is possible to remove the answer for a survey
7. Verify that it is possible to add the answer field for a survey
8. Verify that it is not possible to save the survey with an empty answer field for a survey
9. Verify that it is possible to save the survey with all valid data
10. Verify that it is possible to cancel the survey creation at any stage
11. Verify that it is not possible to edit a published survey
12. Verify that it is possible to edit the Not Published survey
13. Verify that it is possible to delete the Not Published survey

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the tabs on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Examine the tabs on the page|1) There are two tabs - <b>Open</b> and <b>Closed</b>. The <b>Open</b> tab is active by default|

### **#2. Verify the content of the Open tab on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Observe the content of the <b>Open</b> tab|1) There is a table with 3 columns:</br>- Question (text of question)</br>- Status (Published/Not Published)</br>- Responses (amount of users who responded to the survey)|

### **#3. Verify the content of the new Survey form on a Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Examine the content of the <b>Reader pool</b> section|1) The <b>Reader pool</b> section appears on the right side of the Open tab</br>2) There are:</br>- Question text field (required)</br>- Calendar (to select the date range of survey)</br>- Text field for answer with cross icons to remove (required)</br>- the <b>+Add</b> link button (to add new answer variant)</br>- the <b>Save</b> and <b>Cancel</b> buttons|

### **#4. Verify that it is not possible to save survey without question**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Leave the question field empty</br>3) Enter options in the answer fields</br>4) Click <b>Save</b>|4) Validation message appears. The survey is not saved|

### **#5. Verify that it is not possible to select the past dates for the survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Click Calendar</br>3) Select the past date|3)  It is not possible to select the date in the past|

### **#6. Verify that it is possible to remove the answer for a survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) On the right side of an answer, click the delete icon|2) The answer is removed|

### **#7. Verify that it is possible to add the answer field for a survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Click <b>+ Add</b> to add the survey answer|2) Survey answer is added|

### **#8. Verify that it is not possible to save the survey with an empty answer field for a survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Fill in the question field</br>3) Leave the field for answer empty</br>4) Click <b>Save</b>|4) Validation message appears. The survey is not saved|

### **#9. Verify that it is possible to save the survey with all valid data**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Fill in the question field</br>3) Click <b>+Add</b> to add a new answer</br>4) Type a new answer</br>5) Click Calendar and select date range in the future</br>6) Click <b>Save</b>|6) Survey is saved on the <b>Open</b> tab with the <b>Not published</b> state|

### **#10. Verify that it is possible to cancel the survey creation at any stage**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Fill in the question field</br>3) Click <b>+Add</b> to add a new answer</br>4) Type a new answer</br>5) Click Calendar and select date range in the future</br>6) Click <b>Cancel</b>|6) Survey is not saved|

### **#11. Verify that it is not possible to edit a published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey|1) Click published survey|1) In the <b>Reader poll</b> section on the right side, information about the survey appears. There is a name, answers to the survey, and percentage for each answer. No actions appear|

### **#12. Verify that it is possible to edit the Not Published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a not published survey|1) Click not published survey</br>2) In the <b>Reader poll</b> section, click <b>Edit</b></br>3) Edit name</br>4) Edit date range</br>5) Add answer</br>6) Remove any answer</br>7) Click <b>Save</b>|7) All changes are saved and appear in the <b>Open</b> tab as a <b>Not published</b> survey|

### **#13. Verify that it is possible to delete the Not Published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a not published survey|1) Click not published survey</br>2) In the <b>Reader poll</b> section, click <b>Delete</b></br>3) Confirm on the confirmation dialog|2) The survey is removed from the <b>Open</b> tab|

</details>
