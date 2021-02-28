### Back to [Log in and sign up to the portal](../../) feature

# Allow users to log in to the portal using an email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to login with an email and password

## Acceptance criteria

<pre>
<b><i>Scenario: A site user logs in to the portal</i></b>

Given I have an account on the Sports Hub site

When I visit any page on the site
Then I see the <b>Log in</b> button in the upper-right corner of the page

When I click <b>Log in</b>
Then I am taken to the <b>Log in</b> page
  And I see the page with the fields: <b>Email</b>, <b>Password</b>, and the <b>Log in</b> button
  And I see <b>Google+</b> and <b>Facebook</b> icons above the fields
  And I see the link "Forgot password?" above the <b>Password</b> field
  And I see the <b>Get Started</b> button in the upper-right corner of the page, next to the label "Don’t have an account?"

When I entered all the fields on the <b>Log in</b> page and click <b>Log in</b>
Then I am authenticated at the website
  And I am taken to the home page
  And the login link is replaced with my name
  And I see the <b>Log out</b> button in the drop-down menu next to my name
  And I see the <b>View profile</b> item in the drop-down menu next to my name

When I click <b>View profile</b>
Then I am taken to my profile page
  And I see 4 tabs:
    - Personal
    - Change password
    - My surveys
    - Team hub
  And the <b>Personal</b> tab is active and contains my information:
    - My profile picture
    - First name
    - Last name
    - Email
</pre>

## Mockups

1. Users see the <b>Sign Up</b> button
2. Users see the log in form
3. Users see validation errors
4. Users see home page after successful logging in
5. Users see a profile menu
6. Users see a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Sign Up button:**

![Users see the Sign Up button](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/home_page_logged_out_user.png)

**2. Users see the log in form:**

![Users see the log in form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**3. Users see validation errors:**

![Users see validation errors](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_form_validation.png)

**4. Users see home page after successful logging in:**

![Users see home page after successful logging in](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/home_page_logged_in_user.png)

**5. Users see a profile menu:**

![Users see a profile menu](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_menu_for_email_registration.png)

**6. Users see a profile page:**

![Users see a profile page](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_page.png)

</details>

## Test cases

1. Verify that the user is able to log into the Sports Hub site with valid credentials
2. Verify that the user is not able to log into the Sports Hub site with invalid credentials
3. Verify that the user is not able to log into the Sports Hub site with empty boxes for credentials
4. Verify that the user is able to log out from the Sports Hub site

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to log into the Sports Hub site with valid credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Have a site user account registered|1) Click **Log in** in the upper-right corner of the page</br>2) Enter valid data in the **Email address** and **Password** fields</br>3) Click **Log in**|3) The user is successfully logged in|

### **#2. Verify that the user is not able to log into the Sports Hub site with invalid credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Click **Log in** in the upper-right corner of the page</br>2) Enter invalid data in the **Email address** or **Password** fields</br>3) Click **Log in**|3) The user is not able to log in with invalid credentials|

### **#3. Verify that the user is not able to log into the Sports Hub site with empty boxes for credentials**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Click **Log in** in the upper-right corner of the page</br>2) Leave the <b>Email address</b> and <b>Password</b> fields empty</br>3) Click **Log in**|3) The user is not able to log in to the account with invalid credentials|

### **#4. Verify that the user is able to log out from the Sports Hub site**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in|1) Click the drop-down button on the right of the profile picture</br>2) Select **Log out** from the drop-down menu|2) The user is logged out from the Sports Hub site|
</details>
