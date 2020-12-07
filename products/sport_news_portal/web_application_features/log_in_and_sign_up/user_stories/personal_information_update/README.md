### Back to [Log In and Sign Up to the portal](../../) feature

# Allow users to update their personal information

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to update my personal information

## Acceptance criteria

<pre>
Scenario: A site user updates personal information
Given I’m a site user on the personal profile page

When I enter the new information in the <b>First name</b>, <b>Last name</b>, <b>Email</b> fields, and click <b>Update Profile</b>
Then the system saves the changes and immediately updates the user’s name in the page header
  And I see a success message

When I click <b>Update Profile</b> with empty fields, invalid email or photo with invalid format (only .jpg, .png, .jpeg, .tif are allowed)
Then I see an error messages
</pre>

## Mockups

1. User sees a profile page
2. User sees successful update message
3. User sees error message
4. User sees image format validation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a profile page:**

![User sees a profile page](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_page.png)

**2. User sees successful update message:**

![User sees successful update message](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/successful_personal_info_update_message.png)

**3. User sees error message:**

![User sees error message](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/error_message.png)

**4. User sees image format validation popup:**

![User sees image format validation popup](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/image_format_validation.png)

</details>

## Test cases

1. Verify that the user is able to update personal information with an email account
2. Verify that the user is not able to update personal information if signed up with a social network account
3. Verify that the user is not able to update personal information when fields are empty
4. Verify that photo with the invalid format cannot be uploaded

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to update personal information with an email account**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- The user is logged in with an email account|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Change the information in the **First name**, **Last name**, and **Email** fields on the **Personal** tab</br>4) Upload a new photo with a valid format</br>5) Click **Update profile**|4) The system saves the changes and immediately updates the user’s name in the page header|

### **#2. Verify that the user is not able to update personal information if signed up with a social network account**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- The user is logged in with social networks account|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Examine the **Personal** tab on the profile page|3) User is not able to change any personal information|

### **#3. Verify that the user is not able to update personal information when fields are empty**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- The user is logged in with an email account|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Delete the data in the **Last name**, **First name**, and **Email** fields</br>4) Click **Update profile**|4) The user sees the error message that the required fields can not be empty|

### **#4. Verify that photo with the invalid format cannot be uploaded**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- The user is logged in with an email account</br>- Only .jpg, .png, .jpeg, .tif formats are allowed|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Try to upload a profile photo with invalid format|3) User sees the dialog "Only .jpg, .png, .jpeg, .tif formats are allowed"|
</details>
