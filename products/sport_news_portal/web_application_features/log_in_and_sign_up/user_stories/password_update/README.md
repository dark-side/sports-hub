### Back to [Log in and sign up to the portal](../../) feature

# Allow users to change their password via profile

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to update my password

## Acceptance criteria

<pre>
<b><i>Scenario: A site user updates password</i></b>

Given I am a site user on the Change password tab in my profile

And I see a form with three fields:
  - Old password
  - New password
  - Password confirmation

When I enter a new password
Then I see my input as bullets
  And I see an icon that shows me the information I enter

When I enter an old, new password, confirmation password, and click <b>Change Password</b>
Then the system saves the changes and displays a message about success

When I enter the wrong old password and click <b>Change Password</b>
Then I see an error message "Password does not match"

When I enter a new password and confirmation password that do not match, and click <b>Change Password</b>
Then I see an error message "Password does not match"

When I enter a password with an invalid format
Then I see an error message "Use at least 8 characters that includes numbers and letters"
</pre>

## Mockups

1. Users see <b>Change Password</b> form
2. Users see filled out <b>Change Password</b> form
3. Users receive validation messages on <b>Change Password</b> form
4. Users receive a successful update message
5. Users receive an error message

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Change Password form:**

![Users see Change Password form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/change_password_form.png)

**2. Users see filled out Change Password form:**

![Users see filled out Change Password form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/change_password_filled_form.png)

**3. Users receive validation messages on Change Password form:**

![Users receive validation messages on Change Password form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/change_password_validation_messages.png)

**4. Users receive a successful update message:**

![Users receive a successful update message](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/successful_password_update_message.png)

**5. Users receive an error message:**

![Users receive an error message](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/error_message.png)

</details>

## Test cases

1. Verify that the user is able to change the password via profile
2. Verify that the user is not able to change password via profile in case an invalid old password is provided
3. Verify that the user is not able to change the password to the new one with invalid format via profile
4. Verify that the user is not able to change the password via profile when the new password and confirmation password do not match
5. Verify that the user is not able to change the password if they are signed up with social networks

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to change the password via profile**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Select the **Change password** tab on the profile page</br>4) Enter the correct information in the fields</br>5) Click **Change password**|5) The changes are saved and the user receives a success message|

### **#2. Verify that the user is not able to change password via profile in case an invalid old password is provided**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account|1) Click the drop-down button on the right of the profile picture</br>2) Select **Change password** from the drop-down menu</br>3) Enter invalid data in the **Old password** field on the profile page</br>4) Enter the valid data in the **New password** and **Password confirmation** fields</br>5) Click **Change password**|6) The user receives an error message "Password does not match"|

### **#3. Verify that the user is not able to change the password to the new one with invalid format via profile**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account</br>- Password must contain at least 8 characters (letters and numbers)|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Select the **Change password** tab on the profile page</br>4) Enter the valid password in the **Old password** field</br>5) Enter the same invalid password in the **New password** and **Password сonfirmation** fields</br>6) Click **Change password**|6) The user receives an error message "Password must contain at least 8 characters (letters and numbers)"|

### **#4. Verify that the user is not able to change the password via profile when the new password and confirmation password do not match**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account</br>- Password must contain at least 8 characters (letters and numbers)|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Select the **Change password** tab on the profile page</br>4) Enter the valid password in the **Old password** field</br>5) Enter different passwords in the **New password** and **Password сonfirmation** fields</br>6) Click **Change password**|6) The user receives an error message "Passwords do not match"|

### **#5. Verify that the user is not able to change the password if they are signed up with social networks**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with social networks account|1) Click the drop-down button on the right of the profile picture</br>2) Select **View profile** from the drop-down menu</br>3) Examine the available tabs on the profile page|3) The **Change password** tab is not visible|

</details>
