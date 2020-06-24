### Back to [Log In and Sign Up to the portal](../../) feature

# Allow users to log in to the portal using an email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to login with an email and password

## Acceptance criteria

    Scenario: A site user logs in to the portal with an email and password
    Given I have an account in the portal

    When I visit any page on the site
    Then I see a "Log In" button at the top right corner of the page
    When I click on the "Log In" button
    Then I am taken to a Log In page
      And I see a form with the fields: First Name, Last Name, Email, Password, and a Log In button
      And I see Google and Facebook icons above the form
      And I see a link "Forgot password?" above the Password field
      And I see a button "Get Started" next to the text "Don’t have an account?" at the top of the page
    When I complete the login form and click the "Log In" button 
    Then I am authenticated at the web site 
      And I am taken to a Home page
      And the login link is replaced with my name
      And I see a Log Out link in the drop-down menu next to my name
      And I see a link to View Profile in the drop-down menu next to my name
    When I click on View Profile
    Then I am taken to my profile page
      And I see 4 tabs:
        - Personal 
        - Change Password 
        - My Surveys
        - Team Hub
      And the Personal tab is active with a form that contains my information:
        - my avatar
        - First Name
        - Last Name
        - Email

## Mockups

1. User sees Sign Up button
2. User sees Log In form
3. User sees validation errors
4. User sees Home Page after successful log in
5. User sees a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Sign Up button:**

![Home Page Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/home_page_logged_out_user.png)

**2. User sees Log In form:**

![Log In Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**3. User sees validation errors:**

![Log In Form With Validation Errors](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_form_validation.png)

**4. User sees Home Page after successful log in:**

![Home Page Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/home_page_logged_in_user.png)

**5. User sees a profile page:**

![Profile Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_page.png)

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
