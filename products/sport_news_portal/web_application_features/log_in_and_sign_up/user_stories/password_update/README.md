### Back to [Log In and Sign Up to the portal](/../../) feature

# Allow users to change their password via profile

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to update my password

## Acceptance criteria

    Scenario: A site user updates password
    Given I'm a site user on the Change Password tab in my profile

    And I see a form with three fields:
      - old password
      - new password
      - password confirmation
    When I type new password
    Then I see my input as bullets
      And I see an icon that will allow me to see the information I enter
    When I enter an old, new password, password confirmation and click Change Password
    Then the system saves the changes and displays a message about success
    When I enter the wrong old password and click Change Password
    Then I see a validation message "Password does not match"
    When I enter a new password and confirmation that do not match and click Change Password
    Then I see a validation message "Password does not match"
    When I enter a password with not a valid format
    Then I see a validation message "Use at least 8 characters and includes numbers and letters"

## Mockups

1. User sees Change Password form
2. User filled out Change Password form

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Change Password form:**

![Change Password Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/change_password_form.png)

**2. User filled out Change Password form:**

![Change Password Filled Out Form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/change_password_filled_form.png)

</details>

## Test Scenarios

1. Verify the content of the Change Password tab on the user profile page
2. Verify that user can change the password
3. Verify clicking on the icon that allows seeing entered information

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of the Change Password tab on the user profile page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to user’s avatar at the top of the page|
|4|Click on ‘View Profile’ link button|User is navigated to the profile page
|5|Click on Change Password tab|And the systems displays a form with three fields:<br>- old password<br>- new password<br>- password confirmation
|6|Observe the content of Password tab|

### **#2. Verify that user can change the password**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to user's avatar at the top of the page|
|4|Click on View Profile link button|User is navigated to the profile page
|5|Click on Change Password tab |
|6|Fill in the field with correct information|
|7|Click on the password confirmation button|The system saves the changes and displays a message about success

### **#3. Verify clicking on the icon that allows seeing entered information**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user’s avatar at the top of the page|
|4|Click on ‘View Profile’ link button|
|5|Click on Change Password tab|
|6|Fill in the fields|
|7|Click on the icon near the new password field|The entered information is shown

</details>
