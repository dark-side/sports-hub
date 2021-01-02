### Back to [Home page of the portal](../../) feature

# Allow admin user to configure Photo of the Day block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to set up Photo of the day
    So that the site users can see it on the Home page

## Acceptance criteria

<pre>
Scenario: An admin user configures the Photo of the day section
Given I am logged in as an admin user

When I am on the <b>Home</b> configuration page
Then I see <b>Cancel</b> and <b>Save all changes</b> buttons on the top right corner
  And I see the <b>Photo of the day</b> section after the <b>Breakdown</b> section
  And I see the <b>Photo of the day</b> section contains the following:
    - <b>Picture</b> - required field with formats .png, .jpg, .tif, .jpeg
    - <b>Alt.</b> - required
    - <b>Photo title</b> - required
    - <b>Short description</b> - required
    - <b>Author</b> - required
  And I see the <b>Show on the main page</b> toggle is displayed

When I upload some photo of valid format to the <b>Photo of the day</b> section
Then the photo is displayed

When I try to upload some photo of invalid format to the <b>Photo of the day</b> section
Then error message appears and the photo is not loaded

When I click <b>Show on the main page</b> toggle
Then the toggle changes to the <b>Hide on the main page</b>
  And the whole <b>Photo of the day</b> section is not shown for the users on the <b>Home</b> page

When I click <b>Hide on the main page</b> toggle
Then the toggle changes to the <b>Show on the main page</b>
  And the whole <b>Photo of the day</b> section is shown for the users on the <b>Home</b> page

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
2. Admin user hovers over the uploaded photo and sees an icon to upload another photo
3. Admin user sees a Publish button after clicking the Save all changes button
4. Admin user sees a success flash message after clicking the Publish button

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a Home configuration page:**

![Admin user sees a Home configuration page](/products/sport_news_portal/web_application_features/home_page/images/home_configuration.png)

**2. Admin user hovers over the uploaded photo and sees an icon to upload another photo:**

![Admin user hovers over the uploaded photo and sees an icon to upload another photo](/products/sport_news_portal/web_application_features/home_page/images/photo_of_day_hover.png)

**3. Admin user sees a Publish button after clicking the Save all changes button:**

![Admin user sees a Publish button after clicking the Save all changes button](/products/sport_news_portal/web_application_features/home_page/images/home_configuration_publish_button.png)

**4. Admin user sees a success flash message after clicking the Publish button:**

![Admin user sees a success flash message after clicking the Publish button](/products/sport_news_portal/web_application_features/home_page/images/success_publish.png)

</details>

## Test cases

1. Verify that admin is able to cancel all changes of the home page
2. Verify that admin is not able to save changes of the home page when there are validation errors
3. Verify that admin is able to save changes of the home page when there are no validation errors
4. Verify that admin is able to publish changes of the home page
5. Verify that admin is able to add photo to the Photo of the day section
6. Verify that admin is not able to upload photo of invalid format to the Photo of the day section
7. Verify that admin is able to fill in Alt., Photo title, Short description, and Author fields in the Photo of the day section
8. Verify that the Photo of the day section can be hidden for users view
9. Verify that the Photo of the day section can be unhidden for users view

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

### **#5. Verify that admin is able to add photo to the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Photo of the day</b> section|1) In the <b>Photo of the day</b> section, click <b>+Add picture</b></br>2) Choose a photo with the valid format (.jpg, .png, .jpeg, .tif)|2) Selected photo is displayed|

### **#6. Verify that admin is not able to upload photo of invalid format to the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Photo of the day</b> section|1) In the <b>Photo of the day</b> section, click <b>+Add picture</b></br>2) Choose a photo of invalid format (any file except .jpg, .png, .jpeg, .tif)|2) The error message "Only .jpg, .png, .jpeg, .tif formats are allowed" is shown|

### **#7. Verify that admin is able to fill in Alt., Photo title, Short description, and Author fields in the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Photo of the day</b> section|1)In the <b>Photo of the day</b> section, fill in <b>Alt.</b>, <b>Photo title</b>, <b>Short description</b>, and <b>Author</b> fields|1) Entered data are present and ready to be saved and published|

### **#8. Verify that the Photo of the day section can be hidden for users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Photo of the day</b> section</br>- There is <b>Show on the main page</b> toggle|1) Examine the <b>Photo of the day</b> section</br>2) Click <b>Show on the main page</b> toggle|2) Toggle changes to the <b>Hide on the main page</b>. The <b>Photo of the day</b> section is not visible for users|

### **#9. Verify that the Photo of the day section can be unhidden for users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page -> <b>Photo of the day</b> section</br>- There is <b>Hide on the main page</b> toggle|1) Examine the <b>Photo of the day</b> section</br>2) Click <b>Hide on the main page</b> toggle|2) The <b>Photo of the day</b> section is visible for users|

</details>
