### Back to [Surveys on the portal](../../README.md) feature

# Allow admin to create surveys on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to create surveys on the portal

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures surveys on the portal</i></b>

Given I am logged in as an admin user

When I view the site
Then I see the Surveys menu item on the left sidebar menu

When I go to the <b>Surveys</b> configuration page
Then I see <b>Opened</b> and <b>Closed</b> tabs, the <b>Reader Poll</b> section, and <b>+ New Survey</b> button
  And I see the <b>Opened</b> tab contains:
    - Question
    - Status (Not published, Published)
    - Actions (for Published: Close; for Not published: Publish)
    - Responses – the number of people who passed the survey
    - Delete icon for each row
  And I see unpublished surveys are at the top of the list

When I click <b>+ New Survey</b>
Then I see a new survey form on the right side that contains
  - A required text field for a question
  - A calendar icon to select a period for voting, required and cannot be selected for the past date
  - A required input field for the answer option
  - The link button to add one more answer option
  - <b>Cancel</b> and <b>Save</b> buttons

When I enter a new question with options and click <b>Save</b>
Then I see the survey is saved to the database in the <b>Not published</b> status
  And I see a survey question appears at the top of the list on the <b>Opened</b> tab

When I select the <b>Not published</b> survey on the <b>Opened</b> tab
Then I see the survey read-only details in the <b>Reader Poll</b> on the right side
  And I see the <b>Delete</b> and <b>Edit</b> buttons

When I click <b>Edit</b>
Then I see edit form with pre-populated data, the <b>Cancel</b> and <b>Save</b> buttons

When I change any information and click <b>Save</b>
Then I see the updated survey on the <b>Opened</b> tab

When I select the <b>Not published</b> survey and <b>Delete</b> button in the <b>Reader Poll</b>
Then I see a confirmation dialog

When I confirm deletion on the confirmation dialog
Then I see a success message
  And I see the survey is removed from the list

When I hover over the survey on the list
Then I see the delete icon

When I click the delete icon
Then I see a confirmation dialog

When I confirm deletion on the confirmation dialog
Then I see a success message
  And I see the survey is removed from the list

<i>You have two options to render a big list: use pagination or infinite scroll</i>

</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees an <b>Opened</b> tab and published survey in the <b>Reader Poll</b>
2. Admin user clicks <b>+ New Survey</b> and sees a new survey form
3. Admin user sees a calendar to select survey period
4. Admin user sees the unpublished survey in the <b>Reader Poll</b>
5. Admin user edits the unpublished survey in the <b>Reader Poll</b>
6. Admin user sees a delete confirmation pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees an Opened tab and published survey in the Reader Poll:**

![Admin user sees an Opened tab and published survey in the Reader Poll](/web_application_features/surveys/images/admin_surveys_open_tab.png)

**2. Admin user clicks + New Survey and sees a new survey form:**

![Admin user clicks + New Survey and sees a new survey form](/web_application_features/surveys/images/admin_new_survey_form.png)

**3. Admin user sees a calendar to select survey period:**

![Admin user sees a calendar to select survey period](/web_application_features/surveys/images/admin_new_survey_calendar.png)

**4. Admin user sees the unpublished survey in the Reader Poll:**

![Admin user sees the unpublished survey in the Reader Poll](/web_application_features/surveys/images/admin_non_published_survey.png)

**5. Admin user edits the unpublished survey in the Reader Poll:**

![Admin user edits the unpublished survey in the Reader Poll](/web_application_features/surveys/images/admin_edit_non_published_survey.png)

**6. Admin user sees a delete confirmation pop-up window:**

![Admin user sees a delete confirmation pop-up window](/web_application_features/surveys/images/admin_delete_confirmation.png)

</details>

## Test cases

1. Verify the tabs on the <b>Surveys</b> page
2. Verify the content of the <b>Opened</b> tab on the <b>Surveys</b> page
3. Verify the content of the new Survey form on the <b>Surveys</b> page
4. Verify that it is not possible to save the survey without a question
5. Verify that it is not possible to select the past dates for the survey
6. Verify that it is possible to remove the answer from the survey
7. Verify that it is possible to add the answer field for the survey
8. Verify that it is not possible to save the survey with an empty answer field
9. Verify that it is possible to save the survey with all valid data
10. Verify that it is possible to cancel the survey creation at any stage
11. Verify that it is not possible to edit the published survey
12. Verify that it is possible to edit the unpublished survey
13. Verify that it is possible to delete the unpublished survey

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the tabs on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Examine the tabs on the page|1) There are two tabs: <b>Opened</b> and <b>Closed</b>. The <b>Opened</b> tab is active by default|

### **#2. Verify the content of the Opened tab on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Observe the content of the <b>Opened</b> tab|1) There is a table with 3 columns:</br>- Question (text of question)</br>- Status (Published/Not Published)</br>- Responses (amount of users who responded to the survey)|

### **#3. Verify the content of the new Survey form on the Surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Examine the content of the <b>Reader Poll</b> section|1) The <b>Reader Poll</b> section appears on the right side of the <b>Opened</b> tab</br>2) There are:</br>- Question text field (required)</br>- Calendar (to select the date range of survey)</br>- Text field for answer with the cross icon to remove the answer (required)</br>- The <b>+Add</b> link button (to add a new answer variant)</br>- The <b>Save</b> and <b>Cancel</b> buttons|

### **#4. Verify that it is not possible to save the survey without a question**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Leave the question field empty</br>3) Enter options in the answer fields</br>4) Click <b>Save</b>|4) Validation message appears. The survey is not saved|

### **#5. Verify that it is not possible to select the past dates for the survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Click the calendar icon</br>3) Select the past date|3) It is not possible to select the past date|

### **#6. Verify that it is possible to remove the answer from the survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) On the right side of an answer, click the delete icon|2) The answer is removed|

### **#7. Verify that it is possible to add the answer field for the survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Click <b>+ Add</b> to add the survey answer|2) The survey answer is added|

### **#8. Verify that it is not possible to save the survey with an empty answer field**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Fill in the question field</br>3) Leave the field for answer empty</br>4) Click <b>Save</b>|4) Validation message appears. The survey is not saved|

### **#9. Verify that it is possible to save the survey with all valid data**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Fill in the question field</br>3) Click <b>+Add</b> to add a new answer</br>4) Type a new answer</br>5) Click the calendar icon and select date range in the future</br>6) Click <b>Save</b>|6) The survey is saved on the <b>Opened</b> tab with the <b>Not published</b> status|

### **#10. Verify that it is possible to cancel the survey creation at any stage**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click <b>+ New Survey</b></br>2) Fill in the question field</br>3) Click <b>+Add</b> to add a new answer</br>4) Type a new answer</br>5) Click the calendar icon and select date range in the future</br>6) Click <b>Cancel</b>|6) The survey is not saved|

### **#11. Verify that it is not possible to edit the published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey|1) Select the published survey|1) In the <b>Reader poll</b> section on the right side, information about the survey appears. There is a name, answers to the survey, and percentage for each answer. No actions appear|

### **#12. Verify that it is possible to edit the unpublished survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is an unpublished survey|1) Select the unpublished survey</br>2) In the <b>Reader poll</b> section, click <b>Edit</b></br>3) Edit name</br>4) Edit date range</br>5) Add answer</br>6) Remove any answer</br>7) Click <b>Save</b>|7) All changes are saved and appear on the <b>Opened</b> tab as a <b>Not published</b> survey|

### **#13. Verify that it is possible to delete the unpublished survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is an unpublished survey|1) Select the unpublished survey</br>2) In the <b>Reader poll</b> section, click <b>Delete</b></br>3) Confirm on the confirmation dialog|2) The survey is removed from the <b>Opened</b> tab|

</details>
