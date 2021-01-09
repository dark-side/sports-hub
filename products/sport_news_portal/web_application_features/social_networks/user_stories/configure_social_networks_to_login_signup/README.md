### Back to [Social networks on the portal](../../) feature

# Allow admin user to configure social networks for sign up and log in

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure which social networks user can use to sign up and log in

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures which social networks are to be used for following</i></b>

Given I am logged in as an admin user

When I view the social networks configuration page
Then I see three tabs available for configuration: <b>Share</b>, <b>Follow</b>, <b>Log In/Sign Up</b>

When I click on the <b>Log In/Sign Up</b> tab
Then I see the following:
  - <b>Facebook</b> and <b>Google +</b> social networks list that can be used for login/sign up
  - <b>Show/Hide</b> toggle for each specific social network
  - <b>Show section</b> toggle
  All social networks are shown by default

When I click <b>Show</b> toggle for any of the social networks from the list
Then toggle changes to <b>Hide</b>
  And it is no longer shown on the <b>Log in/Sign up</b> page

When I click <b>Hide</b> toggle for any of the social networks from the list
Then toggle changes to <b>Show</b>
  And it is shown on the <b>Log in/Sign up</b> page

When I click the <b>Show section</b> toggle
Then toggle change to <b>Hide section</b>
  And I see the whole <b>Log in/Sign up</b> by social network no longer shown on the site

When I click the <b>Hide section</b> toggle
Then toggle changes to <b>Show section</b>
  And I see the whole <b>Log in/Sign up</b> by social network is shown on the site
</pre>

## Mockups

1. Admin user sees Log in/Sign up configuration page with Show section on
2. Admin user sees Log in/Sign up configuration page with Show section off
3. User sees Login page with social network icons
4. User sees Sign Up page with social network icons
5. User sees Login by Facebook example

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Log in/Sign up configuration page with Show section on:**

![Admin user sees Log in/Sign up configuration page with Show section on](/products/sport_news_portal/web_application_features/social_networks/images/login_signup_configuration_page.png)

**2. Admin user sees Log in/Sign up configuration page with Show section off:**

![Admin user sees Log in/Sign up configuration page with Show section off](/products/sport_news_portal/web_application_features/social_networks/images/login_signup_configuration_page_section_off.png)

**3. User sees Login page with social network icons:**

![User sees Login page with social network icons](/products/sport_news_portal/web_application_features/social_networks/images/login_page_with_social_network_icons.png)

**4. User sees Sign Up page with social network icons:**

![User sees Sign Up page with social network icons](/products/sport_news_portal/web_application_features/social_networks/images/signup_page_with_social_network_icons.png)

**5. User sees Login by Facebook example:**

![User sees Login by Facebook example](/products/sport_news_portal/web_application_features/social_networks/images/login_by_facebook_example.png)

</details>

## Test cases

1. Verify the content of the Login/Sign Up tab on the Social Network page
2. Verify the content of the Login/Sign Up tab on the Social Network page
3. Verify that admin can enable login/sign up social network links for the site users in the Login/Sign Up tab by Hide toggle
4. Verify that admin can hide the Login/Sign Up section by clicking the Show section toggle in Log in/Sign up tab
5. Verify that admin can unhide the Login/Sign Up section by clicking the Hide section toggle in Log in/Sign up tab

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Login/Sign Up tab on the Social Network page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> page -> <b>Log in/Sign up</b> tab|1) Examine the content of the <b>Follow</b> tab|1) There are social networks Facebook and Google +. <b>The Show/Hide</b> toggle to activate/deactivate a specific social network and the <b>Show section</b> toggle|

### **#2. Verify the content of the Login/Sign Up tab on the Social Network page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> page -> <b>Log in/Sign up</b> tab</br>- All social networks are enabled for log in/sign up|1) Click <b>Show</b> toggle to disable any social network from the list</br>2) Log out from admin account</br>3) Examine if disabled the log in/sign up for the needed social network is not visible for users.|1) Toggle changed to <b>Hide</b></br>3) The disabled social network is not available for log in/sign up|

### **#3. Verify that admin can enable login/sign up social network links for the site users in the Login/Sign Up tab by Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> page -> <b>Log in/Sign up</b> tab</br>- Some social networks are disabled for log in/sign up|1) Click <b>Hide</b> toggle to enable any social network from the list</br>2) Log out from admin account</br>3) Examine if enabled the log in/sign up for the needed social network is visible for users.|1) Toggle changed to <b>Show</b></br>3) The enabled social network is available for log in/sign up|

### **#4. Verify that admin can hide the Login/Sign Up section by clicking the Show section toggle in Log in/Sign up tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> page -> <b>Log in/Sign up</b> tab</br>- <b>Show section</b> toggle is shown|1) Click the <b>Show section</b> toggle</br>2) Log out from admin account</br>3) Examine if the Log in/Sign up by social networks section is present|1)  Toggle changed to <b>Hide section</b></br>3) The Login/Sign Up by social networks section is not visible for users|

### **#5. Verify that admin can unhide the Login/Sign Up section by clicking the Hide section toggle in Log in/Sign up tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> page -> <b>Log in/Sign up</b> tab</br>- <b>Hide section</b> toggle is shown|1) Click the <b>Hide section</b> toggle</br>2) Log out from admin account</br>3) Examine if the Log in/Sign up by social networks section is present|1)  Toggle changed to <b>Show section</b></br>3) The Login/Sign Up by social networks section is visible for users|

</details>
