### Back to [Social networks on the portal](../../) feature

# Allow admin user to configure social networks for following

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure which social networks user can follow Sport News on

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures which social networks are to be used for following</i></b>

Given I am logged in as an admin user

When I view the social networks configuration page
Then I see three tabs available for configuration: <b>Share</b>, <b>Follow</b>, <b>Log In/Sign Up</b>

When I click the <b>Follow</b> tab
Then I see the following:
  - <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, <b>Youtube</b> social networks list that can be used to follow the Sport News page on the social networks
  - <b>Show/Hide</b> toggle for each specific social network
  - <b>Show section</b> toggle
  All social networks are shown by default

When I click <b>Show</b> toggle for any of the social networks from the list
Then toggle changes to <b>Hide</b>
  And it is no longer shown in the navigation menu for users

When I click <b>Hide</b> toggle for any of the social networks from the list
Then toggle changes to <b>Show</b>
  And it is shown in the navigation menu for users

When I click the <b>Show section</b> toggle
Then toggle change to <b>Hide section</b>
  And the whole <b>Follow</b> section is no longer shown in the navigation menu for users

When I click the <b>Hide section</b> toggle
Then toggle change to <b>Show section</b>
  And the whole <b>Follow</b> section is shown on the navigation menu for users
</pre>

## Mockups

1. Admin user sees Follow configuration page with Show section on
2. Admin user sees Follow configuration page with Show section off
3. User sees Follow icons in the navigation menu

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Follow configuration page with Show section on:**

![Admin user sees Follow configuration page with Show section on](/products/sport_news_portal/web_application_features/social_networks/images/following_configuration_page.png)

**2. Admin user sees Follow configuration page with Show section off:**

![Admin user sees Follow configuration page with Show section off](/products/sport_news_portal/web_application_features/social_networks/images/following_configuration_page_section_off.png)

**3. User sees Follow icons in the site header:**

![User sees Follow icons in the navigation menu](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test cases

1. Verify the content of the Follow tab on a Social Network page
2. Verify that admin can disable following social network links for the site users in the Follow tab by Show toggle
3. Verify that admin can enable following social network links for the site users in the Follow tab by Hide toggle
4. Verify that admin can hide the Follow section by click the Show section toggle on the Follow tab
5. Verify that admin can unhide the Follow section by clicking the Hide section toggle on the Follow tab

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Follow tab on a Social Network page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page|1) Examine the content on the <b>Follow</b> tab|1) There is the social network list: <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, <b>Youtube</b>. The <b>Show/Hide</b> toggle to activate/deactivate a specific social network and the <b>Show section</b> toggle|

### **#2. Verify that admin can disable following social network links for the site users in the Follow tab by Show toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Follow</b> tab</br>- All social networks are enabled for following|1) Click <b>Show</b> toggle for any social network from the list</br>2) Log out from admin account</br>3) Log in by user account</br>4) Check if the disabled social network is not visible for the site user|1) Toggle changed to <b>Hide</b></br>4) The disabled social network is not available for following|

### **#3. Verify that admin can enable following social network links for the site users in the Follow tab by Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Follow</b> tab</br>- Some social networks are disabled for following|1) Click <b>Hide</b> toggle for any social network from the list</br>2) Log out from admin account</br>3) Log in by user account</br>4) Examine if enabled following social network is visible for site users|1) Toggle changed to <b>Show</b></br>4) The enabled social network is available for following|

### **#4. Verify that admin can hide the Follow section by click the Show section toggle on the Follow tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Follow</b> tab</br>- <b>Show section</b> toggle is shown|1) Click <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Follow</b> section is present|1) Toggle changed to <b>Hide section</b></br>4) The <b>Follow</b> section is not visible for users|

### **#5. Verify that admin can unhide the Follow section by clicking the Hide section toggle on the Follow tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Follow</b> tab</br>- <b>Hide section</b> is shown|1) Click <b>Hide section</b> toggle</br>2) Log out from admin account</br>3) Log in by user account</br>4) Check if the <b>Follow</b> section is present|1) Toggle changed to <b>Show section</b></br>4) The <b>Follow</b> section is visible for users|

</details>
