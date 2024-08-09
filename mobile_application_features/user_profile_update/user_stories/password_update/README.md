### Back to [User personal cabinet](../../README.md) feature

# Allow users to change their password via profile

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to update my password

## Acceptance criteria

<pre>
<b><i>Scenario: A user updates password</i></b>

Given I am a user on the Change password page

And I see a form with Change password button and three fields:
  - Old password
  - New password
  - Password confirmation

When I enter a new password
Then I see my input as bullets
  And I see an icon that shows me the information I enter

When I enter an old, new password, confirmation password, and then tap <b>Change Password</b>
Then the system saves the changes and displays a message about success

When I enter the wrong old password and tap <b>Change Password</b>
Then I see the error message "Password does not match"

When I enter a new password and confirmation password that do not match and tap <b>Change Password</b>
Then I see the error message "Password does not match"

When I enter a password with an invalid format
Then I see the error message "Use at least 8 characters that includes numbers and letters"
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Change Password</b> form
2. Users receive validation messages on <b>Change Password</b> form
3. Users receive a successful update message

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Change Password form:**

![Users see Change Password form](/mobile_application_features/user_profile_update/images/application_change_password_form.png)

**2. Users receive validation messages on Change Password form:**

![Users receive validation messages on Change Password form](/mobile_application_features/user_profile_update/images/application_change_password_validation_messages.png)

**3. Users receive a successful update message:**

![Users receive a successful update message](/mobile_application_features/user_profile_update/images/application_successful_password_update_message.png)

</details>

## Test cases

1. Verify that the user is able to change the password via profile
2. Verify that the user is not able to change the password via profile in case an invalid old password is provided
3. Verify that the user is not able to change the password to the new one with invalid format via profile
4. Verify that the user is not able to change the password via profile when the new password and confirmation password do not match
5. Verify that the user is not able to change the password if they are signed up with social networks

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to change the password via profile**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account|1) Tap the profile icon</br>2) Tap the <b>Change password</b> menu item</br>3) Enter the correct information in the fields</br>4) Tap <b>Change password</b>|4) The changes are saved and the user receives a success message|

### **#2. Verify that the user is not able to change the password via profile in case an invalid old password is provided**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account|1) Tap the profile icon</br>2) Tap the <b>Change password</b> menu item</br>3) Enter invalid data in the <b>Old password</b> field on the profile page</br>4) Enter the valid data in the <b>New password</b> and <b>Password confirmation</b> fields</br>5) Tap <b>Change password</b>|5) The user receives an error message "Password does not match"|

### **#3. Verify that the user is not able to change the password to the new one with invalid format via profile**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with an email account</br>- Password must contain at least 8 characters (letters and numbers)|1) Tap the profile icon</br>2) Tap the <b>Change password</b> menu item</br>3) Enter the valid password in the <b>Old password</b> field</br>4) Enter the same invalid password in the <b>New password</b> and <b>Password сonfirmation</b> fields</br>5) Tap <b>Change password</b>|5) The user receives an error message "Password must contain at least 8 characters (letters and numbers)"|

### **#4. Verify that the user is not able to change the password via profile when the new password and confirmation password do not match**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with email account</br>- Password must contain at least 8 characters (letters and numbers)|1) Tap the profile icon</br>2) Tap the <b>Change password</b> menu item</br>3) Enter the valid password in the <b>Old password</b> field</br>4) Enter different passwords in the <b>New password</b> and <b>Password сonfirmation</b> fields</br>5) Tap <b>Change password</b>|5) The user receives an error message "Passwords do not match"|

### **#5. Verify that the user is not able to change the password if they are signed up with social networks**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in with social networks account|1) Tap the profile icon</br>2) Examine the available items in the menu|2) The <b>Change password</b> item is not visible|
</details>
