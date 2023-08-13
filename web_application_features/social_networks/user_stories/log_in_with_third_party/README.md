### Back to [Social networks on the portal](../../README.md) feature

# Allow users to log in to the portal using a third-party authentication provider

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to log in using a third-party authentication provider

## Acceptance criteria

<pre>
<b><i>Scenario: A site user logs in using Facebook or Google+</i></b>

Given I have registered to the portal with Facebook or Google+ account

When I visit the <b>Log in</b> page
Then I see the Google+ and Facebook icons above the form

When I click <b>Google+</b> or <b>Facebook</b>
Then I see my name provided by a selected third-party authentication provider instead of <b>Log in</b> and <b>Log out</b> buttons in the drop-down menu next to my name

When I click the drop-down menu next to my name
Then I see information about the social network I used to log in
  And I see <b>My surveys</b>, <b>Team hub</b>, and <b>Log out</b> items

When I click <b>My surveys</b>
Then I am taken to the <b>My surveys</b> page
  And I see 2 tabs:
    - My surveys
    - Team hub
  And <b>My surveys</b> tab is active
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the log-in form
2. Registered via third party users see a profile menu
3. Registered via third party users see a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the log-in form:**

![Users see the log-in form](/web_application_features/social_networks/images/log_in_empty_form.png)

**2. Registered via third party users see a profile menu:**

![Registered via third party users see a profile menu](/web_application_features/social_networks/images/user_profile_menu_for_third_party.png)

**3. Registered via third party users see a profile page:**

![Registered via third party users see a profile page](/web_application_features/social_networks/images/user_profile_third_party_login.png)

</details>

## Test cases

1. Verify that the user is able to log in to the Sports Hub site using social networks accounts

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to log in to the Sports Hub site using social networks accounts**

|Preconditions|Steps|Expected result
------|-------|----------
|- The user is registered in Google+ or Facebook account</br>- The user is signed up with Google+ or Facebook account</br>- The user is not logged in to the site|1) Go to the **Log in** page</br>2) Click **Google+** or **Facebook**</br>3) Click **Continue with account**|3) The user is logged in with **Google+** or **Facebook** credentials|

</details>
