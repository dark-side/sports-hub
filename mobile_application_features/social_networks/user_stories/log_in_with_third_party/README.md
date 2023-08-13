### Back to [Social networks on the application](../../README.md) feature

# Allow users to log in the application using a third-party authentication provider

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to log in using a third-party authentication provider

## Acceptance criteria

<pre>
<b><i>Scenario: A user logs in using Facebook or Google</i></b>

Given I have registered to the application with Facebook or Google account

When I visit the <b>Log in</b> page
Then I see the Google and Facebook icons above the form

When I tap <b>Google</b> or <b>Facebook</b>
Then I am logged in to the application

When I tap the drop-down profile menu icon
Then I see information about the social network I used to log in
And I see <b>My surveys</b>, <b>Team hub</b>, and <b>Log out</b> menu items
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Log In</b> and <b>Sign Up</b> buttons
2. Users see the log-in form
3. Users see home page after successful logging in
4. Registered via third party users see a profile menu

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Log In and Sign Up buttons:**

![Users see the Log In and Sign Up buttons](/mobile_application_features/social_networks/images/application_user_profile_menu_logged_out.png)

**2. Users see the log-in form:**

![Users see the log-in form](/mobile_application_features/social_networks/images/application_log_in_form.png)

**3. Users see home page after successful logging in:**

![Users see home page after successful logging in](/mobile_application_features/social_networks/images/application_main_articles_section.png)

**4. Registered via third party users see a profile menu:**

![Registered via third party users see a profile menu](/mobile_application_features/social_networks/images/application_user_profile_menu_logged_with_third_party.png)

</details>

## Test cases

1. Verify that the user is able to log in the application using social networks accounts

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to log in the application using social networks accounts**

|Preconditions|Steps|Expected result
------|-------|----------
|- The user is registered in Google or Facebook account</br>- The user is signed up with Google or Facebook account</br>- The user is not logged in to the application|1) Go to the **Log in** page</br>2) Tap **Google** or **Facebook**</br>3) Tap **Continue with account**|3) The user is logged in with **Google** or **Facebook** credentials|
</details>
