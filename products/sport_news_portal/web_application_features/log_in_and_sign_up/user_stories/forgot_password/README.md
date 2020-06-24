### Back to [Log In and Sign Up to the portal](../../) feature

# Allow users to reset their password

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to reset my password

## Acceptance criteria

    Scenario: A site user resets the password
    Given I have an account in the portal

    When I visit a Log In page
    Then I see a link to "Forgot password?"  above the Password field
    When I click the link "Forgot password?" 
    Then I am taken to a Forgot Password page
      And I see an Email field, "Request reset link" button, and a link "Back to Log In"
    When I fill in the form and click on "Request reset link" button
    Then I see "Check your email" message
    When I check my email
      And I see a "Reset Password" button inside
    When I click the button "Reset Password"
    Then I am taken to "Please enter your new password" page
      And I see a form with the fields: New Password, Confirm Password and "Set New Password" button
    When I complete the form and click the "Set New Password" button
    Then I am taken to a Log In page 
      And I see a message "Your password has been updated"

## Mockups

1. User sees Log In form
2. User sees Forgot Password form
3. User sees Check your email screen
4. User sees an email with reset password link
5. User sees Reset Password form
6. User sees Log In form

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Log In form:**

![Log In Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**2. User sees Forgot Password form:**

![Forgot Password Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/forgot_password_empty_form.png)

**3. User sees Check your email screen:**

![Check your email Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/check_your_email_to_reset_password.png)

**4. User sees an email with reset password link:**

![Email Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/check_your_email_to_reset_password.png)

**5. User sees Reset Password form:**

![Reset Password Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/reset_password_form.png)

**6. User sees Log In form:**

![Login Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_form_password_is_updated.png)

</details>

## Test Scenarios

1. Verify "Forgot password" button
2. Verify receiving a mail with a button to Reset Password
3. Verify message "Your password has been updated" after setting new password

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify "Forgot password" button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for email and password, and a login button
|3|Click on "Forgot password" button|User will navigate "Forgot password" page

### **#2. Verify receiving a mail with a button to Reset Password**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for email and password, and a login button
|3|Click on "Forgot password" button|User will navigate "Forgot password" page
|4|Type your email in the field|
|5|Click on "Request reset link" button|
|6|Check your email|Mail with button to Reset Password is received

### **#3. Verify message "Your password has been updated" after setting new password**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for email and password, and a login button
|3|Click on "Forgot password" button|User will navigate "Forgot password" page
|4|Type your email in the field|
|5|Click on "Request reset link" button|
|6|Check your email|Mail with button to Reset Password is received
|7|Click on Reset Password button|User is navigated to "Please enter your new password" page
|8|Fill in New Password, Confirm Password fields|
|9|Click on ‘Set New Password’ button|Message "Your password has been updated" appears

</details>
