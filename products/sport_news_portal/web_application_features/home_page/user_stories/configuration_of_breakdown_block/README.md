### Back to [Home page of the portal](../../) feature

# Allow admin user to configure a breakdown block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to set up Breakdown section news for a specific category
    So that the site users can see them on the home page

## Acceptance criteria

<pre>
Scenario: An admin user configures Breakdown section news for a specific category
Given I am logged as an admin user

When I am on the <b>Home</b> configuration page
Then I see <b>Cancel</b> and <b>Save all changes</b> buttons on the top right corner
  And I see I see an empty <b>Breakdown</b> section under the <b>Main articles</b> section
  And I see <b>Add one more breakdown</b> button
  And I see <b>Show on the main page</b> toggle

When I click <b>Add one more breakdown</b>
  Then I see the form is added in <b>Breakdown</b> section:
    - <b>Category</b> - contains a list of all sports categories, first category from the list is selected by default, is required
    - <b>Conference</b> - contains a list of all conferences, nothing is selected by default
    - <b>Team</b> - contains a list of all teams, nothing is selected by default
    - <b>Delete</b> button
    - <b>Add one more breakdown</b> button

When I change the default category
Then I see the <b>Conference</b> drop-down list is updated with conferences from the selected category
  And I see the <b>Team</b> drop-down list is updated with teams according to the selected category

When I select <b>Conference</b>
Then I see the <b>Team</b> drop-down list is updated with teams according to the selected conference 

When I click <b>Delete</b>
Then the confirmation popup appears

When I click <b>Yes</b> on the confirmation popup
Then I see the row is removed from the page

When I click <b>Show on the main page</b> toggle
Then the toggle changes to the <b>Hide on the main page</b>
  And the whole <b>Breakdown</b> section is not shown for the users on the <b>Home</b> page

When I click <b>Hide on the main page</b> toggle
Then the toggle changes to the <b>Show on the main page</b>
  And the whole <b>Breakdown</b> section is shown for the users on the <b>Home</b> page

When I click the <b>Cancel</b> button
Then I see all changes which were made are canceled

When I click the <b>Save all changes</b> button and there are validation errors
Then I see all changes are present and there are validation errors highlighted

When I click the <b>Save all changes</b> button and there are no validation errors
Then all changes are saved and I see the <b>Publish</b> button

When I click the <b>Publish</b> button
Then the <b>Home</b> page is in the published state
  And I see a success flash message
  And I see <b>Cancel</b> and <b>Save all changes</b> buttons on the top right corner
</pre>

## Mockups

1. Admin user sees a Home configuration page
2. Admin user sees a Publish button after clicking the Save all changes button
3. Admin user sees a success flash message after clicking the Publish button

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a Home configuration page:**

![Admin user sees a Home configuration page](/products/sport_news_portal/web_application_features/home_page/images/home_configuration.png)

</details>

**2. Admin user sees a Publish button after clicking the Save all changes button:**

![Admin user sees a Publish button after clicking the Save all changes button](/products/sport_news_portal/web_application_features/home_page/images/home_configuration_publish_button.png)

**3. Admin user sees a success flash message after clicking the Publish button:**

![Admin user sees a success flash message after clicking the Publish button](/products/sport_news_portal/web_application_features/home_page/images/success_publish.png)

## Test cases

1. Verify that admin is able to cancel all changes of the home page
2. Verify that admin is not able to save changes of the home page when there are validation errors
3. Verify that admin is able to save changes of the home page when there are no validation errors
4. Verify that admin is able to publish changes of the home page
5. Verify that the admin is able to add Breakdown in the Breakdown section
6. Verify that the admin is able to change Category in the Breakdown section
7. Verify that admin is able to select a Conference in the Breakdown section
8. Verify that admin is able to select a Team in the Breakdown section
9. Verify that it is possible to delete a Breakdown in the Breakdown section
10. Verify that it is possible to delete the last Breakdown from the Breakdown section
11. Verify that the Breakdown section can be hidden for users view
12. Verify that the Breakdown section can be unhidden for users view

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to cancel all changes of the home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page</br>- There are some unpublished changes|1) Click <b>Cancel</b> button|1) All changes are canceled|

### **#2. Verify that admin is not able to save changes of the home page when there are validation errors**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page|1) Leave required fields empty</br>2) Click the <b>Save all changes</b> button|2) Error messages about empty required fields appear. All changes are present but not saved|

### **#3. Verify that admin is able to save changes of the home page when there are no validation errors**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page|1) Fill in all required fields</br>2) Click the <b>Save all changes</b> button|2) All changes are saved. <b>Publish</b> button appears|

### **#4. Verify that admin is able to publish changes of the home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page</br>- Changes are saved|1) Click <b>Publish</b> button|1) <b>Home</b> page is in published state|

### **#5. Verify that the admin is able to add Breakdown in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section|1) Click <b>Add one more breakdown</b> in the <b>Breakdown</b> section|1) The <b>Breakdown</b> form is added with:</br> - <b>Category</b> (required with selected by default first category form the list)</br>- <b>Conference</b> (empty)</br>- <b>Team</b> (empty) dropdown lists</br>- <b>Delete</b> button|

### **#6. Verify that the admin is able to change Category in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section</br>- <b>Breakdown</b> is added|1) Change the sports category in the <b>Breakdown</b> section</br>2) Check if the <b>Conference</b> and <b>Team</b> drop-down lists are updated|2) The <b>Conference</b> and <b>Team</b> drop-down lists are updated according to the selected category|

### **#7. Verify that admin is able to select a Conference in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section</br>- <b>Breakdown</b> is added</br>- <b>Category</b> is selected|1) In the <b>Breakdown</b> section, select a <b>Conference</b></br>2) Check if the <b>Team</b> drop-down list is updated|2) The <b>Team</b> drop-down list is updated according to the selected conference|

### **#8. Verify that admin is able to select a Team in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section</br>- <b>Breakdown</b> is added</br>- <b>Category</b> is selected</br>- <b>Conference</b> is selected|1) In the <b>Breakdown</b> section, select a <b>Team</b>|1) The <b>Team</b> is selected|

### **#9. Verify that it is possible to delete a Breakdown in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section|1) In the Breakdown section, click <b>Delete</b> any breakdown</br>2) Click <b>Yes</b> on the confirmation popup|2) The breakdown is deleted|

### **#10. Verify that it is possible to delete the last Breakdown from the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section</br>- There is only 1 breakdown present|1) In the Breakdown section, go to the last breakdown, and then click <b>Delete</b></br>2) Click <b>Yes</b> on the confirmation popup|2) The breakdown is deleted|

### **#11. Verify that the Breakdown section can be hidden for users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section</br>- There is <b>Show on the main page</b> toggle|1) Examine the <b>Breakdown</b> section</br>2) Click <b>Show on the main page</b> toggle|2) Toggle changes to the <b>Hide on the main page</b>. The <b>Breakdown</b> section is not visible for users|

### **#12. Verify that the Breakdown section can be unhidden for users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Breakdown</b> section</br>- There is <b>Hide on the main page</b> toggle|1) Examine the <b>Breakdown</b> section</br>2) Click <b>Hide on the main page</b> toggle|2) Toggle changes to the <b>Show on the main page</b>. The <b>Breakdown</b> section is visible for users|

</details>
