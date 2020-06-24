### Back to [Log In and Sign Up to the portal](../../) feature

# Allow users to log in to the portal using a third-party authentication provider

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to login using a third-party authentication provider

## Acceptance criteria

    Scenario: A site user logins using Facebook or Google
    Given I have registered to the portal with Facebook or Google account

    When I visit the login page of the site
    Then I see Google and Facebook icons above the form
      And when I click on the Google or Facebook icons
    Then I see my name provided by selected third-party authentication provider instead of Login link and Log out link in the drop-down menu next to my name
    When I click on the drop-down menu next to my name
    Then I see information about provider I used to login
      And I see My Surveys, Team Hub, and Log Out links
    When I click on My Surveys
    Then I am taken to my My Surveys page
      And I see 2 tabs:
        - My Surveys
        - Team Hub
      And My Surveys is active

## Mockups

1. User views Log In form
2. User views a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. User views Log In form:**

![Log In Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**2. User views a profile page:**

![Profile Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_third_party_login.png)

</details>

## Test Scenarios

1. Verify log in link at the top of the page on the site
2. Verify that click on the "Log in" I will take the user to a Login page
3. Verify that the user is be able to login with valid credentials
4. Verify that the user is not able to login with invalid credentials
5. Verify that the user is not able to login with empty credentials fields
6. Verify "Get started" button
7. Verify a "Back to Sign in" button
8. Verify navigating to the user's profile page
9. Verify the content of the profile page
10. Verify the content of the personal tab on the profile page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify log in link at the top of the page on the site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Observe the top right corner of the page|Button "Get Started" next to the text "Don’t have an account?" at the top of the page is placed

### **#2. Verify that click on the "Log in" I will take the user to a Login page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|User is redirected to the Login page with fields for my email and password, and a login button appears

### **#3. Verify that the user is be able to login with valid credentials**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for my email and password, and a login button
|3|Type valid data in email address and password fields|User is successfully logged in

### **#4. Verify that the user is not able to login with invalid credentials**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for my email and password, and a login button
|3|Type valid data in email address and password fields|User cannot log in because email and password are invalid

### **#5. Verify that the user is not able to login with empty credentials fields**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Click on "Log in" button|Login page with fields for my email and password, and a login button
|3|Type valid data in email address and password fields|User cannot log in with empty email and password fields

### **#6. Verify "Get started" button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|On the log in page examine "Get started?" button|"Get started" button is present
|3|Click on "Get started" button|User will be taken to "Create Account" page

### **#7. Verify a "Back to Sign in" button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|"Get started" button is present|Login page with fields for email and password, and a login button
|3|Click on "Log  in" button|
|4|Click on "Forget password" button|User will navigate the "Forgot password" page
|5|Verify the "Back to Sign in" link|"Back to Sign in" link is present

### **#8. Verify navigating to the user's profile page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user's avatar at the top of the page|
|4|Click on "View Profile" link button|User is navigated to the profile page

### **#9. Verify the content of the profile page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user's avatar at the top of the page|
|4|Click on "View Profile" link button|
|5|Check the tabs on the profile page|There should be 4 tabs on the profile page:<br>- Personal<br>- Change Password<br>- My Surveys<br>- Team Hub

### **#10. Verify the content of the personal tab on the profile page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user's avatar at the top of the page|
|4|Click on "View Profile" link button|
|5|Check the content of the personal tab|There should contain such information:<br>- User's avatar<br>- First Name<br>- Last Name<br>- Email

</details>
