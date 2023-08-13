### Back to [Home page of the portal](../../README.md) feature

# Allow admin user to configure the Photo of the day section

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to set up Photo of the day
    So that site users can see it on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures the Photo of the day section</i></b>

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

When I click the <b>Show on the main page</b> toggle
Then the toggle changes to <b>Hide on the main page</b>
  And the whole <b>Photo of the day</b> section is not shown for users on the <b>Home</b> page

When I click the <b>Hide on the main page</b> toggle
Then the toggle changes to <b>Show on the main page</b>
  And the whole <b>Photo of the day</b> section is shown for users on the <b>Home</b> page

When I click the <b>Cancel</b> button
Then I see all changes are canceled

When I click the <b>Save all changes</b> button and there are validation errors
Then I see all changes are present and there are validation errors highlighted

When I click the <b>Save all changes</b> button and there are no validation errors
Then all changes are saved and I see the <b>Publish</b> button

When I click the <b>Publish</b> button
Then the <b>Home</b> page is in the published state
  And I see a success flash message
  And I see <b>Cancel</b> and <b>Save all changes</b> buttons on the top right corner
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Home</b> configuration page
2. Admin user hovers over the uploaded photo and sees an icon to upload another photo
3. Admin user sees the <b>Publish</b> button after clicking the <b>Save all changes</b> button
4. Admin user sees a success flash message after clicking the <b>Publish</b> button

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Home configuration page:**

![Admin user sees the Home configuration page](/web_application_features/home_page/images/home_configuration.png)

**2. Admin user hovers over the uploaded photo and sees an icon to upload another photo:**

![Admin user hovers over the uploaded photo and sees an icon to upload another photo](/web_application_features/home_page/images/photo_of_day_hover.png)

**3. Admin user sees the Publish button after clicking the Save all changes button:**

![Admin user sees the Publish button after clicking the Save all changes button](/web_application_features/home_page/images/home_configuration_publish_button.png)

**4. Admin user sees a success flash message after clicking the Publish button:**

![Admin user sees a success flash message after clicking the Publish button](/web_application_features/home_page/images/success_publish.png)

</details>

## Test cases

1. Verify that admin is able to cancel all changes on the <b>Home</b> page
2. Verify that admin is not able to save changes on the <b>Home</b> page when there are validation errors
3. Verify that admin is able to save changes on the <b>Home</b> page when there are no validation errors
4. Verify that admin is able to publish changes on the <b>Home</b> page
5. Verify that admin is able to add photo to the <b>Photo of the day</b> section
6. Verify that admin is not able to upload photo of invalid format to the <b>Photo of the day</b> section
7. Verify that admin is able to fill in <b>Alt.</b>, <b>Photo title</b>, <b>Short description</b>, and <b>Author</b> fields in the <b>Photo of the day</b> section
8. Verify that the <b>Photo of the day</b> section can be hidden from users
9. Verify that the <b>Photo of the day</b> section can be visible to users

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to cancel all changes on the Home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page</br>- There are some unpublished changes|1) Click <b>Cancel</b>|1) All changes are canceled|

### **#2. Verify that admin is not able to save changes on the Home page when there are validation errors**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page|1) Leave required fields empty</br>2) Click the <b>Save all changes</b> button|2) Error messages about empty required fields appear. All changes are present but not saved|

### **#3. Verify that admin is able to save changes on the Home page when there are no validation errors**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page|1) Fill in all required fields</br>2) Click the <b>Save all changes</b> button|2) All changes are saved. The <b>Publish</b> button appears|

### **#4. Verify that admin is able to publish changes on the Home page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page</br>- Changes are saved|1) Click <b>Publish</b>|1) The <b>Home</b> page is in published state|

### **#5. Verify that admin is able to add photo to the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Photo of the day</b> section|1) In the <b>Photo of the day</b> section, click <b>+Add picture</b></br>2) Choose a photo with the valid format (.jpg, .png, .jpeg, .tif)|2) Selected photo is displayed|

### **#6. Verify that admin is not able to upload photo of invalid format to the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Photo of the day</b> section|1) In the <b>Photo of the day</b> section, click <b>+Add picture</b></br>2) Choose a photo of invalid format (any file except .jpg, .png, .jpeg, .tif)|2) The error message "Only .jpg, .png, .jpeg, .tif formats are allowed" appears|

### **#7. Verify that admin is able to fill in Alt., Photo title, Short description, and Author fields in the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Photo of the day</b> section|1) In the <b>Photo of the day</b> section, fill in <b>Alt.</b>, <b>Photo title</b>, <b>Short description</b>, and <b>Author</b> fields|1) Entered data are present and ready to be saved and published|

### **#8. Verify that the Photo of the day section can be hidden from users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Photo of the day</b> section</br>- There is the <b>Show on the main page</b> toggle|1) Examine the <b>Photo of the day</b> section</br>2) Click the <b>Show on the main page</b> toggle|2) The toggle changes to <b>Hide on the main page</b>. The <b>Photo of the day</b> section is not visible to users|

### **#9. Verify that the Photo of the day section can be visible to users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Photo of the day</b> section</br>- There is the <b>Hide on the main page</b> toggle|1) Examine the <b>Photo of the day</b> section</br>2) Click the <b>Hide on the main page</b> toggle|2) The <b>Photo of the day</b> section is visible to users|

</details>
