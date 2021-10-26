### Back to [Log in and sign up in the application](../../) feature

# Allow users to sign up using a third-party authentication provider

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a new user
    I want to be able to sign up using a third-party authentication provider
    So that I will be on the Sports Hub members list

## Acceptance criteria

<pre>
<b><i>Scenario: A new user creates or has an already created personal account on Facebook or Google</i></b>

Given I have a Facebook or Google account

When I visit the <b>Google</b> Account or Log in page
Then I see Google and Facebook icons above the form

When I tap the <b>Google</b> or Facebook icon
Then I see access confirmation dialog with a confirmation button

When I tap Confirm
Then the dialog is closed
  And I am logged in to the application

When I tap the drop-down profile menu
Then I see information about the social network I used to sign up
  And I see <b>My surveys</b>, <b>Team hub</b>, and <b>Log out</b> menu items
</pre>

## Mockups

1. Users see the <b>Log In</b> and <b>Sign Up</b> buttons
2. Users see the <b>Create Account</b> page
3. Users see home page after successful sign up
4. Registered via third party users see a profile menu

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Log In and Sign Up buttons:**

![Users see the Log In and Sign Up buttons](/products/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_menu_logged_out.png)

**2. Users see the Create Account page:**

![Users see the Create Account page](/products/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_sing_up_form.png)

**3. Users see home page after successful sign up:**

![Users see home page after successful sign up](/products/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_main_articles_section.png)

**4. Registered via third party users see a profile menu:**

![Registered via third party users see a profile menu](/products/sports_hub_portal/mobile_application_features/log_in_and_sign_up/images/application_user_profile_menu_logged_with_third_party.png)

</details>

## Test cases

1. Verify that the user is signed up using Google profile
2. Verify that the user is signed up using Facebook profile

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is signed up using Google profile**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account</br>- Google profile is created|1) Tap **Log in**</br>2) Select the **Google** icon above sign up form</br>3) On the confirmation dialog box, tap **Confirm**|3) The dialog box is closed and I am logged in via **Google** profile|

### **#2. Verify that the user is signed up using Facebook profile**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is not logged in to the account</br>- Facebook profile is created|1) Tap **Log in**</br>2) Select the **Facebook** icon above sign up form</br>3) On the confirmation dialog box, tap **Confirm**|3) The dialog box is closed and I am logged in via **Facebook** profile|
</details>
