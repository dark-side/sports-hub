### Back to [Log In and Sign Up to the portal](/../../) feature

# Allow users to sign up and log in with a third-party authentication provider

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a new user
    I want to be able to sign up using a third-party authentication provider

## Acceptance criteria

    Scenario: A new user creates a personal account using Facebook or Google
    Given I have Facebook or Google account

    When I visit the Create Account or Log In page
    Then I see Google and Facebook icons above the form
    When I click on the Google or Facebook icon
    Then I see access confirmation popup with a confirmation button
    When I click on the Confirm button
    Then the popup is closed
      And I see my name provided by selected third-party authentication provider instead of Log in link and Log out link in the drop-down menu next to my name
    When I click on the drop-down menu next to my name
    Then I see information about provider I used to sign up
      And I see My Surveys, Team Hub, and Log Out links
    When I click on My Surveys
    Then I am taken to my My Surveys page
      And I see 2 tabs:
        - My Surveys
        - Team Hub
      And My Surveys is active

## Mockups

1. User views a Create Account page
2. User views Log In form
3. User views a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. User views a Create Account page:**

![Sign Up Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/sing_up_empty_form.png)

**2. User views Log In form:**

![Log In Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**3. User views a profile page:**

![Profile Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_third_party_login.png)

</details>

## Test Scenarios

1. Verify sign up using Google profile
2. Verify sign up using Facebook profile

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify sign up using Google profile**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for email and password, and a login button
|3|Observe Google icon above sign up form|Access confirmation popup with a confirmation button
|4|Click on Google icon|A popup will be closed and I will see my name provided by selected third-party authentication provider instead of Login link and Log out link in the drop-down menu next to my name
|5|Click on the Confirm button appears|

### **#2. Verify sign up using Facebook profile**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for email and password, and a login button
|3|Observe Facebook icon above sign up form|Access confirmation popup with a confirmation button appears
|4|Click on Facebook icon|A popup will be closed and I will see my name provided by Facebook provider instead of Login link and Log out link in the drop-down menu next to my name
|5|Click on the Confirm button|

</details>
