### Back to [Home page of the portal](../../) feature

# Allow admin user to configure main articles block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to set up up to 5 main articles
    So that the site users can see them on the home page

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures the Main articles section on the home page</i></b>

Given I am logged in as an admin user

When I am on the <b>Home</b> configuration page
Then I see <b>Cancel</b> and <b>Save all changes</b> buttons on the top right corner
  And I see the <b>Main articles</b> section on the top of the page
  And I see the <b>Main articles</b> section contains a form with the followingfields:
    - <b>Category</b> - contains a list of all sports categories, first category from the list is selected by default, is required
    - <b>Conference</b> - contains a list of all conferences, nothing is selected by default
    - <b>Team</b> - contains a list of all teams, nothing is selected by default
    - <b>Article</b> - contains a list of all articles from the category, is required
    - <b>Add one more article</b> button
    - <b>Show on the main page</b> toggle

When I add one more article
Then <b>Delete</b> button appears for both present articles form

When I click <b>Delete</b>
Then the confirmation popup appears

When I click <b>Yes</b> on the confirmation popup
Then I see the row is removed from the page
  And the <b>Delete</b> button is not shown for the last article form

When I click on the <b>Add one more article</b> button four times
Then the <b>Add one more article</b> button disappears

When I click <b>Show on the main page</b> toggle on any of the artocle form
Then the <b>Show on the main page</b> changes to <b>Hide on the main page</b>

When I change the category in the drop-down
Then I see the <b>Conference</b> drop-down list is updated with conferences from the selected category
  And I see the <b>Team</b> drop-down list is updated with teams according to the selected category
  And I see the <b>Article</b> drop-down list is updated with articles according to the selected category

When I select <b>Conference</b>
Then I see the <b>Team</b> drop-down list is updated with teams according to the selected conference 
  And I see the <b>Article</b> drop-down list is updated with articles according to the selected conference

When I select <b>Team</b>
  Then I see the <b>Article</b> drop-down list is updated with articles according to the selected team

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

**2. Admin user sees a Publish button after clicking the Save all changes button:**

![Admin user sees a Publish button after clicking the Save all changes button](/products/sport_news_portal/web_application_features/home_page/images/home_configuration_publish_button.png)

**3. Admin user sees a success flash message after clicking the Publish button:**

![Admin user sees a success flash message after clicking the Publish button](/products/sport_news_portal/web_application_features/home_page/images/success_publish.png)

</details>

## Test cases

1. Verify that admin is able to cancel all changes of the home page
2. Verify that admin is not able to save changes of the home page when there are validation errors
3. Verify that admin is able to save changes of the home page when there are no validation errors
4. Verify that admin is able to publish changes of the home page
5. Verify that the admin is able to change Category in the Main articles section
6. Verify that admin is able to select a Conference in the Main articles section
7. Verify that admin is able to select a Team in the Main articles section
8. Verify that it is possible to add a new article in the Main articles section
9. Verify that maximum 5 articles can be added in the Main articles section
10. Verify that it is possible to delete an article from the Main articles section
11. Verify that it is not possible to delete the last article from the Main articles section
12. Verify that it is not possible to hide the Main articles section

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

### **#5. Verify that the admin is able to change Category in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page|1) Change the sports category in the Main articles section</br>2) Check if the <b>Conference</b>, <b>Team</b>, and <b>Article</b> drop-down lists are updated|2) The <b>Conference</b>, <b>Team</b>, and <b>Article</b> drop-down lists are updated according to the selected category|

### **#6. Verify that admin is able to select a Conference in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page</br>- <b>Category</b> is selected|1) In the <b>Main articles</b> section, select a <b>Conference</b></br>2) Check if <b>Team</b> and <b>Article</b> drop-down lists are updated|2) The <b>Team</b> and <b>Article</b> drop-down lists are updated according to the selected conference|

### **#7. Verify that admin is able to select a Team in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page</br>- <b>Category</b> is selected</br>- <b>Conference</b> is selected|1) In the <b>Main articles</b> section, select a <b>Team</b></br>2) Check if <b>Article</b> drop-down list is updated|2) The <b>Article</b> drop-down list is updated according to the selected team|

### **#8. Verify that it is possible to add a new article in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Main articles</b> section|1) In the <b>Main articles</b> section, click <b>Add one more article </b>|1) Drop-down lists to save a new article appear (<b>Category</b> (required), <b>Conference</b>, <b>Team</b>, <b>Article</b> (required))|

### **#9. Verify that maximum 5 articles can be added in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Main articles</b> section</br>- There is 1 article|1) In the <b>Main articles</b> section, click <b>Add one more article </b></br>2) Repeat steps 1 for 3 more times|2) Fields for 5 new articles appear. The <b>Add one more article </b> is not shown|

### **#10. Verify that it is possible to delete an article from the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Main articles</b> section</br>- There is more than one article|1) In the <b>Main articles</b> section, select any article, and then click <b>Delete</b></br>2) Click <b>Yes</b> on the confirmation popup|2) The article form is deleted|

### **#11. Verify that it is not possible to delete the last article from the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Main articles</b> section</br>- There are 2 articles|1) In the <b>Main articles</b> section, select any article, and then click <b>Delete</b></br>2) Click <b>Yes</b> on the confirmation popup|2) The article form is deleted. The <b>Delete</b> button is not shown for the last article form|

### **#12. Verify that it is not possible to hide the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Main articles</b> section|1) Examine the <b>Main articles</b> section|1) There is no show/hide toggle for the <b>Main articles</b> section,so it can’t be hidden for the users|

</details>
