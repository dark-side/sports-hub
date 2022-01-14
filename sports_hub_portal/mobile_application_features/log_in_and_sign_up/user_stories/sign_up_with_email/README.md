### Back to [Log in and sign up in the application](../../) feature

# Allow users to sign up in the application using an email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a new user
    I want to be able to sign up using my email
    So that I will be on the Sports Hub members list

## Acceptance criteria

<pre>
<b><i>Scenario: A new user creates a personal account using an email</i></b>

When I visit the <b>Log in</b> page
Then I see the <b>Get Started</b> link in the upper-right corner of the page

When I tap <b>Get Started</b>
Then I am taken to the <b>Create Account</b> page
  And I see the page with the boxes: <b>First name</b>, <b>Last name</b>, <b>Email</b>, <b>Password</b>, and the <b>Sign up</b> button
  And I see the <b>Google</b> and <b>Facebook</b> icons below the <b>Create Account</b> label
  And I see the <b>Log in</b> button in the upper-right corner of the page next to the label "Already have an account?" on the left

When on the sign-up page I entered an invalid email address, and then tap <b>Sign up</b>
Then I see the error message "Please enter valid email"

When on the sign-up page I entered an invalid password, and tap <b>Sign up</b>
Then I see the error message "Password must contain at least 8 characters (letters and numbers)"

When I complete the sign-up form with valid data and then tap <b>Sign up</b>
Then I am taken to the <b>Log in</b> page

When I check my email
Then I see a registration confirmation letter and the <b>Go to website button</b>

When I tap <b>Go to website</b>
Then I am taken to the <b>Log in</b> page

</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Log In</b> and <b>Sign Up</b> buttons
2. Users see the <b>Create Account</b> page
3. Users receive an email about successful registration
4. Users see the log-in form
5. Users see home page after successful logging in
6. Users see a profile menu

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Log In and Sign Up buttons:**

![Users see the Log In and Sign Up buttons](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_menu_logged_out.png)

**2. Users see the Create Account page:**

![Users see the Create Account page](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_sing_up_form.png)

**3. Users receive an email about successful registration:**

![Users receive an email about successful registration](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/email_successful_sing_up.png)

**4. Users see the log-in form:**

![Users see the log-in form](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_log_in_form.png)

**5. Users see home page after successful logging in:**

![Users see home page after successful logging in](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_main_articles_section.png)

**6. Users see a profile menu:**

![Users see a profile menu](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_menu_logged_with_email.png)

</details>

## Test cases

1. Verify that the user is signed up after completing the form correctly
2. Verify that the user is not signed up if they provide already used email address
3. Verify that the user is not signed up if registration was not confirmed
4. Verify that the user is not signed up with empty required fields
5. Verify that the user is not signed up with an invalid password
6. Verify that the user is not signed up with an invalid email

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is signed up after completing the form correctly**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account|1) In the upper-right corner of the page, tap **Get Started**</br>2) Enter valid data in all required fields on the **Create Account** page</br>3) Tap **Sign Up**</br>4) Check the entered email inbox</br>5) In the subscription confirmation email, tap **Go to website**|4) The user receives the subscription confirmation email</br>5) The user goes to the **Log in** page and is able to log in to the application with the data used to sign up|

### **#2. Verify that the user is not signed up if they provide already used email address**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account</br>- The user already has an account on the Sports Hub|1) Tap **Get Started**</br>2) Enter valid data in all required fields on the **Create Account** page</br>3) Enter the email of an already registered user</br>4) Tap **Sign up**|4) The user receives the message that the email address is already in use|

### **#3. Verify that the user is not signed up if registration was not confirmed**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account|1) Tap **Get Started**</br>2) Enter valid data in all required fields on the **Create Account** page</br>3) Tap **Sign up**</br>4) Check your email</br>5) Do not confirm registration </br>6) Go to the <b>Log in</b> page</br>7) Try to log in with credentials used to sign up|4) The user receives an email about successful registration</br>7) The user is not able to log in|

### **#4. Verify that the user is not signed up with empty required fields**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account|1) Tap **Get started**</br>2) Leave the required fields empty on the **Create Account** page</br>3) Tap **Sign up**|3) The user receives a message that all required fields should not be empty|

### **#5. Verify that the user is not signed up with an invalid password**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account</br>-Password must contain at least 8 characters (letters and numbers)|1) Tap **Get Started**</br>2) Enter valid data in all required fields on the **Create Account** page</br>3) Type the password that contains less than 8 characters, does not contain letters, or contains only letters or numbers</br>4) Tap **Sign up**|4) The message "_Password must contain at least 8 characters (letters and numbers)_" appears|

### **#6. Verify that the user is not signed up with an invalid email**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account|1) Tap **Get Started**</br>2) Enter valid data in all required fields on the **Create Account** page</br>3) Enter an invalid email address</br>4) Tap **Sign up**|4) The message "_Please enter valid email_" appears|
</details>
