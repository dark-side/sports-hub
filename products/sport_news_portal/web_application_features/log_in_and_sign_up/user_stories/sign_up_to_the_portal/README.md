### Back to [Log In and Sign Up to the portal](../../) feature

# Allow users to sign up to the portal using an email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a new user
    I want to be able to sign up using my email
    So that I will be in the site member list

## Acceptance criteria

    Scenario: A new user creates a personal account using an email

    When I visit any page on the site
    Then I see a "Sign Up" button at the top right corner of the page
    When I click on the "Sign Up" button
    Then I am taken to a Create Account page
      And I see a form with the fields: First Name, Last Name, Email, Password, and a Sign Up button
      And I see Google and Facebook icons above the form
      And I see a "Log In" button next to the text "Already have an account?" at the top of the page
    When I complete the sign up form with an invalid email and click the "Sign Up" button
    Then I see a validation field error "Please enter valid email"
    When I complete the sign up form with invalid password and click the "Sign Up" button
    Then I see a validation field error "Password must contain at least 8 characters (letters and numbers)"
    When I complete the sign up form with valid data and click the "Sign Up" button
    Then I am taken to a Log In form
    When I check my email
    Then I see a confirmation about successful registration and "Go To Website" button
    When I click on "Go To Website" button
    Then I am taken to a Log In form

## Mockups

1. User is logged out and sees Sign Up button
2. User is on a Create Account page
3. User received an email about successful registration
4. User sees Log In form

<details>
  <summary>Click here to see mockups details</summary>

**1. User is logged out and sees Sign Up button:**

![Home Page Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/home_page_logged_out_user.png)

**2. User is on a Create Account page:**

![Sign Up Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/sing_up_empty_form.png)

**3. User received an email about successful registration:**

![Email Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/email_successful_sing_up.png)

**4. User sees Log In form:**

![Log In Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

</details>

## Test Scenarios

1. Verify all needed fields and buttons on a Create Account page
2. Verify sign up after completing the form

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify all needed fields and buttons on a Create Account page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|On the login page examine "Get started" button|"Don't have an account?" button is present
|3|Click on "Don't have an account?"" button|User will be taken to "Create Account" page
|4|Examine "Create Account" page|Fields for my First Name, Last Name, email, password, and a Sign Up button should be present

### **#2. Verify sign up after completing the form**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Click on "Don't have an account?" button|User will be taken to "Create Account" page
|3|Examine "Create Account" page|Fields for my First Name, Last Name, email, password, and a Sign Up button should be present
|4|Fill out all requested fields|
|5|Click the Sign Up button|A message to "Check your email <email@email.com>" appears
|6|Check your email|A confirmation about successful registration is received

</details>
