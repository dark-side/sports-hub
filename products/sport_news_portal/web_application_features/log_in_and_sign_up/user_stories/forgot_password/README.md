### Back to [Log in and sign up to the portal](../../) feature

# Allow users to reset their password

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to reset my password

## Acceptance criteria

<pre>
<b><i>Scenario: A site user resets the password</i></b>

Given I have an account on the portal

When I visit the <b>Log in</b> page
Then I see the link "Forgot password?" above the <b>Password</b> field

When I click the link "Forgot password?"
Then I am taken to the <b>Forgot password</b> page
  And I see the <b>Email</b> fiels, the <b>Request reset link</b> button and the <b>Back to Log In</b> link

When I enter email address and click the <b>Request reset link</b>
Then I see the message "Check your email"

When I check my email
Then I see the <b>Reset password</b> button inside

When I click <b>Reset password</b>
Then I am taken to the <b>Please enter your new password</b> page
  And I see the fields: <b>New password</b>, <b>Confirm password</b>, and the <b>Set new password</b> button

When I complete the form and click <b>Set new password</b>
Then I am taken to the <b>Log in</b> page
  And I see the message "Your password has been updated"
</pre>

## Mockups

1. User sees Log In form
2. User sees Forgot Password form
3. User sees Check your email screen
4. User sees an email with reset password link
5. User sees Reset Password form
6. User sees Log In form with password updated message

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Log In form:**

![User sees Log In form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**2. User sees Forgot Password form:**

![User sees Forgot Password form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/forgot_password_empty_form.png)

**3. User sees Check your email screen:**

![User sees Check your email screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/check_your_email_to_reset_password.png)

**4. User sees an email with reset password link:**

![User sees an email with reset password link](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/email_reset_password.png)

**5. User sees Reset Password form:**

![User sees Reset Password form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/reset_password_form.png)

**6. User sees Log In form with password updated message:**

![User sees Log In form with password updated message](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_form_password_is_updated.png)

</details>

## Test cases

1. Verify that the user is able to update the password
2. Verify that the user is not able to update a password if the Confirm password field is empty
3. Verify that the user is able to cancel the password update procedure after clicking on the Forgot password link and still can use old credentials
4. Verify that the user is able to cancel the password update procedure on the Enter new password page and still can use old credentials

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to update the password**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- User is registered in the system|1) Click **Log in**</br>2) Click on the "Forgot password?" link</br>3) Enter your email</br>4) Click **Request reset link**</br>5) Check your email</br>6) Click Reset password</br>7) Enter the new password in the **New password** and **Confirm password** fields</br>8) Click **Change password**</br>9) Enter old credentials</br>10) Click **Log in**</br>11) Enter new credentials</br>12) Click **Log in**|8) User is redirected to the **Log in** page and sees the message "Your password has been updated"</br>10) User is not logged in. Message about invalid credentials appears</br>12) User is logged in|

### **#2. Verify that the user is not able to update a password if the Confirm password field is empty**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- User is registered in the system|1) Click **Log in**</br>2) Click on the **Forgot password?** link</br>3) Enter your email</br>4) Click **Request reset link**</br>5) Check your email</br>6) Click **Reset Password**</br>7) Enter the new password in the **New password** field</br>8) Do not enter the new password in the **Confirm password** field</br>9) Click **Set new password**|9) The user sees the error message that the required fields can not be empty|

### **#3. Verify that the user is able to cancel the password update procedure after clicking on the Forgot password link and still can use old credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- User is registered in the system|1) Click **Log in**</br>2) Click on the **Forgot password?** link</br>3) Enter your email</br>4) Click Back to log in</br>5) Enter old credentials</br>6) Click Log in|4) The **Log in** page is opened</br>6) User is logged in|

### **#4. Verify that the user is able to cancel the password update procedure on the Enter new password page and still can use old credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- User is registered in the system|1) Click **Log in**</br>2) Click on the **Forgot password?** link</br>3) Enter your email</br>4) Click **Request reset link**</br>5) Check your email</br>6) Click **Reset password**</br>7) Click **Back to log in**</br>8) Enter old credentials</br>9) Click **Log in**|7) The **Log in** page opens</br>9) User is logged in|
</details>
