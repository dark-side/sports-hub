### Back to [Log in and sign up to the portal](../../) feature

# Allow users to log in to the portal using a third-party authentication provider

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to login using a third-party authentication provider

## Acceptance criteria

<pre>
<b><i>Scenario: A site user logs in using Facebook or Google+</i></b>

Given I have registered to the portal with Facebook or Google+ account

When I visit the <b>Log in</b> page
Then I see the Google+ and Facebook icons above the form

When I click <b>Google+</b> or <b>Facebook</b>
Then I see my name provided by a selected third-party authentication provider instead of <b>Log in</b> and <b>Log out</b> buttons in the drop-down menu next to my name

When I click the drop-down icon next to my name
Then I see information about the social network I used to log in
  And I see <b>My surveys</b>, <b>Team hub</b>, and <b>Log out</b> items

When I click <b>My surveys</b>
Then I am taken to the <b>My surveys</b> page
  And I see 2 tabs:
    - My surveys
    - Team hub
  And <b>My surveys</b> is active
</pre>

## Mockups

1. User sees Log In form
2. Registered via third party user sees a profile menu
3. Registered via third party user sees a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Log In form:**

![User sees Log In form](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/log_in_empty_form.png)

**2. Registered via third party user sees a profile menu:**

![Registered via third party user sees a profile menu](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_menu_for_third_party.png)

**3. Registered via third party user sees a profile page:**

![Registered via third party user sees a profile page](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_third_party_login.png)

</details>

## Test cases

1. Verify that the user is able to log into the Sport News site using social networks accounts

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to log into the Sport News site using social networks accounts**

|Preconditions|Steps|Expected result
------|-------|----------
|- User is registered in Google+ or Facebook account</br>- User is signed up with Google+ or Facebook account</br>- Not logged in to the site|1) Go to the **Log in** page</br>2) Click **Google+** or **Facebook**</br>3) Click **Continue with account**|3) User is logged in with **Google+** or **Facebook** credentials|

</details>
