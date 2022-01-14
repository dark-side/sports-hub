### Back to [Log in and sign up in the application](../../) feature

# Allow users to reset their password

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to reset my password

## Acceptance criteria

<pre>
<b><i>Scenario: A user resets the password</i></b>

Given I have an account in the application

When I visit the <b>Log in</b> page
Then I see the link "Forgot password?" above the Password field

When I select the "Forgot password?" link
Then I am taken to the <b>Forgot password</b> page
  And I see the <b>Email</b> field, the <b>Request reset link</b> button and the <b>Back to Log In</b> link

When I enter email address and select the <b>Request reset link</b>
Then I see the message "Check your email"

When I check my email
Then I see the <b>Reset password</b> button inside

When I tap <b>Reset password</b>
Then I am taken to the <b>Please enter your new password</b> page
  And I see the fields: <b>New password</b>, <b>Confirm password</b>, and the <b>Log in</b> button

When I complete the form and click <b>Log in</b>
Then I am logged in and taken to the home page
  And the password has been updated
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the log-in form
2. Users see the <b>Forgot Password</b> form
3. Users see <b>Check your email</b> screen
4. Users receive an email with reset password link
5. Users see the <b>Reset Password</b> form

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the log-in form:**

![Users see the log-in form](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_log_in_form.png)

**2. Users see the Forgot Password form:**

![Users see the Forgot Password form](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_forgot_password_form.png)

**3. Users see Check your email screen:**

![Users see Check your email screen](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_check_your_email_to_reset_password.png)

**4. Users receive an email with reset password link:**

![Users receive an email with reset password link](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/email_reset_password.png)

**5. Users see the Reset Password form:**

![Users see the Reset Password form](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_reset_password_form.png)

</details>

## Test cases

1. Verify that the user is able to update the password
2. Verify that the user is not able to update a password if the <b>Confirm password</b> field is empty
3. Verify that the user is able to cancel the password update procedure after selecting the <b>Forgot password</b> link and still can use old credentials
4. Verify that the user is able to cancel the password update procedure on the <b>Enter new password</b> page and still can use old credentials

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to update the password**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is registered in the system|1) Tap **Log in**</br>2) Select the **Forgot password?** link</br>3) Enter your email</br>4) Select the **Request reset link**</br>5) Check your email</br>6) Tap **Reset password**</br>7) Enter the new password in the **New password** and **Confirm password** fields</br>8) Tap **Change password**</br>9) Enter old credentials</br>10) Tap **Log in**</br>11) Enter new credentials</br>12) Tap **Log in**|8) The user is redirected to the **Log in** page and receives the message "Your password has been updated"</br>10) The user is not logged in. Message about invalid credentials appears</br>12) The user is logged in|

### **#2. Verify that the user is not able to update a password if the Confirm password field is empty**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is registered in the system|1) Tap **Log in**</br>2) Select the **Forgot password?** link</br>3) Enter your email</br>4) Select the **Request reset link**</br>5) Check your email</br>6) Tap **Reset Password**</br>7) Enter the new password in the **New password** field</br>8) Do not enter the new password in the **Confirm password** field</br>9) Tap **Log in**|9) The user receives the error message that the required fields can not be empty|

### **#3. Verify that the user is able to cancel the password update procedure after selecting the Forgot password link and still can use old credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is registered in the system|1) Tap **Log in**</br>2) Select the **Forgot password?** link</br>3) Enter your email</br>4) Tap **Back to log in**</br>5) Enter old credentials</br>6) Tap **Log in**|4) The **Log in** page opens</br>6) The user is logged in|

### **#4. Verify that the user is able to cancel the password update procedure on the Enter new password page and still can use old credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is registered in the system|1) Tap **Log in**</br>2) Select the **Forgot password?** link</br>3) Enter your email</br>4) Select the **Request reset link**</br>5) Check your email</br>6) Tap **Reset password**</br>7) Tap **Back to log in**</br>8) Enter old credentials</br>9) Tap **Log in**|7) The **Log in** page opens</br>9) The user is logged in|
</details>
