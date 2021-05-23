### Back to [Social networks on the portal](../../) feature

# Allow admin user to configure social networks for sign up and log in

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure which social networks users can use to sign up and log in

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures social networks that can be used to log in/sign up</i></b>

Given I am logged in as an admin user

When I view the <b>Social networks</b> configuration page
Then I see three tabs available for configuration: <b>Share</b>, <b>Follow</b>, <b>Log in/Sign up</b>

When I select the <b>Log in/Sign up</b> tab
Then I see the following:
  - <b>Facebook</b> and <b>Google +</b> social networks list that can be used to log in/sign up
  - The <b>Show/Hide</b> toggle for each specific social network
  - The <b>Show section</b> toggle
  All social networks are shown by default

When I click the <b>Show</b> toggle for any of the social networks from the list
Then the toggle changes to <b>Hide</b>
  And it is no longer shown on the <b>Log in/Sign up</b> page

When I click the <b>Hide</b> toggle for any of the social networks from the list
Then the toggle changes to <b>Show</b>
  And it is shown on the <b>Log in/Sign up</b> page

When I click the <b>Show section</b> toggle
Then the toggle changes to <b>Hide section</b>
  And I see the whole <b>Log in/Sign up</b> by social network no longer shown on the site

When I click the <b>Hide section</b> toggle
Then the toggle changes to <b>Show section</b>
  And I see the whole <b>Log in/Sign up</b> by social network is shown on the site
</pre>

## Mockups

1. Admin user sees <b>Log in/Sign up</b> configuration page with <b>Show section</b> on
2. Admin user sees <b>Log in/Sign up</b> configuration page with <b>Show section</b> off
3. Users see <b>Log in</b> page with social network icons
4. Users see <b>Sign up</b> page with social network icons
5. Users see Log in with Facebook example

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Log in/Sign up configuration page with Show section on:**

![Admin user sees Log in/Sign up configuration page with Show section on](/products/sports_hub_portal/web_application_features/social_networks/images/login_signup_configuration_page.png)

**2. Admin user sees Log in/Sign up configuration page with Show section off:**

![Admin user sees Log in/Sign up configuration page with Show section off](/products/sports_hub_portal/web_application_features/social_networks/images/login_signup_configuration_page_section_off.png)

**3. Users see Log in page with social network icons:**

![Users see Log in page with social network icons](/products/sports_hub_portal/web_application_features/social_networks/images/login_page_with_social_network_icons.png)

**4. Users see Sign up page with social network icons:**

![Users see Sign up page with social network icons](/products/sports_hub_portal/web_application_features/social_networks/images/signup_page_with_social_network_icons.png)

**5. Users see Log in with Facebook example:**

![Users see Log in with Facebook example](/products/sports_hub_portal/web_application_features/social_networks/images/login_by_facebook_example.png)

</details>

## Test cases

1. Verify the content of the <b>Log in/Sign up</b> tab on the <b>Social networks</b> page
2. Verify the content of the <b>Log in/Sign up</b> tab on the <b>Social networks</b> page
3. Verify that admin can enable log in/sign up social network links for site users on the <b>Log in/Sign up</b> tab by the <b>Hide</b> toggle
4. Verify that admin can hide the <b>Log in/Sign up</b> section by clicking the <b>Show section</b> toggle on the <b>Log in/Sign up</b> tab
5. Verify that admin can unhide the <b>Log in/Sign up</b> section by clicking the <b>Hide section</b> toggle on the <b>Log in/Sign up</b> tab

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Log in/Sign up tab on the Social networks page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> page > <b>Log in/Sign up</b> tab|1) Examine the content of the <b>Follow</b> tab|1) There are social networks Facebook and Google +, the <b>Show/Hide</b> toggle to activate/deactivate a specific social network and the <b>Show section</b> toggle|

### **#2. Verify the content of the Log in/Sign up tab on the Social networks page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> page > <b>Log in/Sign up</b> tab</br>- All social networks are enabled to log in/sign up|1) Click the <b>Show</b> toggle to disable any social network from the list</br>2) Log out of admin account</br>3) Examine if disabled the log in/sign up for the needed social network is not visible for users|1) The toggle changes to <b>Hide</b></br>3) The disabled social network is not available to log in/sign up|

### **#3. Verify that admin can enable log in/sign up social network links for site users on the Log in/Sign up tab by the Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> page > <b>Log in/Sign up</b> tab</br>- Some social networks are disabled to log in/sign up|1) Click the <b>Hide</b> toggle to enable any social network from the list</br>2) Log out of admin account</br>3) Examine if enabled log in/sign up for the needed social network is visible for users|1) The toggle changes to <b>Show</b></br>3) The enabled social network is available to log in/sign up|

### **#4. Verify that admin can hide the Log in/Sign up section by clicking the Show section toggle on the Log in/Sign up tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> page > <b>Log in/Sign up</b> tab</br>- The <b>Show section</b> toggle is shown|1) Click the <b>Show section</b> toggle</br>2) Log out of admin account</br>3) Examine if the Log in/Sign up with social networks section is present|1) The toggle changes to <b>Hide section</b></br>3) The Log in/Sign up with social networks section is not visible to users|

### **#5. Verify that admin can unhide the Log in/Sign up section by clicking the Hide section toggle on the Log in/Sign up tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> page > <b>Log in/Sign up</b> tab</br>- The <b>Hide section</b> toggle is shown|1) Click the <b>Hide section</b> toggle</br>2) Log out of admin account</br>3) Examine if the Log in/Sign up with social networks section is present|1) The toggle changes to <b>Show section</b></br>3) The Log in/Sign up with social networks section is visible to users|

</details>
