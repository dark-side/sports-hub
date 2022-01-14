### Back to [Log in and sign up in the application](../../) feature

# Allow users to log in to the application using an email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to log in with an email and password

## Acceptance criteria

<pre>
<b><i>Scenario: A user logs in to the application</i></b>

Given I have an account on the Sports Hub

When I visit any page
Then I see the <b>Log in</b> button in the upper-right corner of the page

When I tap <b>Log in</b>
Then I am taken to the <b>Log in</b> page
  And I see the page with the fields: <b>Email</b>, <b>Password</b>, and the <b>Log in</b> button
  And I see <b>Google</b> and <b>Facebook</b> icons above the fields
  And I see the link "Forgot password?" above the <b>Password</b> field
  And I see the <b>Get Started</b> link in the upper-right corner of the page, next to the label "Don’t have an account?"

When I fill in all the fields on the <b>Log in</b> page and tap <b>Log in</b>
Then I am authenticated in the application
  And I am taken to the home page
  And I see the profile menu icon

When I tap the profile menu icon
Then I see my name
  And I see next items in the drop-down profile menu:
    - Personal
    - Change password
    - My surveys
    - Team hub
    - Log out

When I tap <b>Personal</b>
Then I am taken to the <b>Personal</b> page
  And the <b>Personal</b> page contains my information:
    - My profile picture
    - First name
    - Last name
    - Email

When I tap <b>Log out</b>
Then I am logged out from the application
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Log In</b> and <b>Sign Up</b> buttons
2. Users see the log-in form
3. Users see home page after successful logging in
4. Users see a profile menu
5. Users see a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Log In and Sign Up buttons:**

![Users see the Log In and Sign Up buttons](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_menu_logged_out.png)

**2. Users see the log-in form:**

![Users see the log-in form](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_log_in_form.png)

**3. Users see home page after successful logging in:**

![Users see home page after successful logging in](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_main_articles_section.png)

**4. Users see a profile menu:**

![Users see a profile menu](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_menu_logged_with_email.png)

**5. Users see a profile page:**

![Users see a profile page](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_page.png)

</details>

## Test cases

1. Verify that the user is able to log in to the application with valid credentials
2. Verify that the user is not able to log in to the application with invalid credentials
3. Verify that the user is not able to log in to the application with empty fields for credentials
4. Verify that the user is able to log out from the application

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to log in to the application with valid credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Have a user account registered|1) Tap **Log in** in the upper-right corner of the page</br>2) Enter valid data in the **Email address** and **Password** fields</br>3) Tap **Log in**|3) The user is successfully logged in|

### **#2. Verify that the user is not able to log in to the application with invalid credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Tap **Log in** in the upper-right corner of the page</br>2) Enter invalid data in the **Email address** or **Password** fields</br>3) Tap **Log in**|3) The user is not able to log in with invalid credentials|

### **#3. Verify that the user is not able to log in to the application with empty fields for credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Tap **Log in** in the upper-right corner of the page</br>2) Leave the <b>Email address</b> and <b>Password</b> fields empty</br>3) Tap **Log in**|3) The user is not able to log in to the account with invalid credentials|

### **#4. Verify that the user is able to log out from the application**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in|1) Tap the profile icon</br>2) Select **Log out** from the drop-down menu|2) The user is logged out from the application|
</details>
