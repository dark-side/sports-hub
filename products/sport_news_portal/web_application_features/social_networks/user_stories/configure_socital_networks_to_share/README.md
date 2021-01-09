### Back to [Social networks on the portal](../../) feature

# Allow admin user to configure social networks for sharing

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure which social networks user can use to share the Sport News site

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures which social networks are to be used for sharing</i></b>

Given I am logged in as an admin user

When I view the social networks configuration page
Then I see three tabs available for configuration: <b>Share</b>, <b>Follow</b>, <b>Log In/Sign Up</b>

When I am on the <b>Share</b> tab
Then I see the following:
  - <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b> social networks list that can be used for sharing a Sport News page
  - <b>Show/Hide</b> toggle for each specific social network
  - <b>Show section</b> toggle
  And all social networks are shown by default

When I click <b>Show</b> toggle for any of the social networks from the list
Then toggle changes to <b>Hide</b>
  And it is no longer shown in the header section for the users

When I click <b>Hide</b> toggle for any of the social networks from the list
Then toggle changes to <b>Show</b>
  And it is shown in the header section for the users

When I click the <b>Show section</b> toggle
Then toggle changes to <b>Hide section</b>
  And the whole <b>Share</b> section is no longer shown in the site header for users

When I click the <b>Hide section</b> toggle
Then toggle changes to <b>Show section</b>
  And the whole share section is shown in the site header for users
</pre>

## Mockups

1. Admin user sees Share configuration page with Show section on
2. Admin user sees Share configuration page with Show section off
3. User sees Share icons in the site header

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Share configuration page with Show section on:**

![Admin user sees Share configuration page with Show section on](/products/sport_news_portal/web_application_features/social_networks/images/sharing_configuration_page.png)

**2. Admin user sees Share configuration page with Show section off:**

![Admin user sees Share configuration page with Show section off](/products/sport_news_portal/web_application_features/social_networks/images/sharing_configuration_page_section_off.png)

**3. User sees Share icons in the site header:**

![User sees Share icons in the site header](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test cases

1. Verify the tabs on a Social Network page
2. Verify the content of the Share tab on a Social Networks page
3. Verify that admin can disable sharing social network links in the Share tab by Show toggle
4. Verify that admin can enable sharing social network links for the site users in the Share tab by Hide toggle
5. Verify that admin can hide the Share section by click on the Show section toggle on the Share tab
6. Verify that admin can unhide the Share section by click on the Hide section toggle on the Share tab

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the tabs on a Social Network page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page|1) Examine the tabs on the page|1) There are three tabs: <b>Share</b>, <b>Follow</b>, <b>Login/Sign Up</b>. The <b>Share</b> tab is active by default|

### **#2. Verify the content of the Share tab on a Social Networks page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page|1) Examine the content of <b>Share</b> tab|1) There is a social network list: <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, <b>Youtube</b>. The <b>Show/Hide</b> toggle to activate/deactivate a social network and the <b>Show section</b> toggle.|

### **#3. Verify that admin can disable sharing social network links in the Share tab by Show toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Share</b> tab|1) Click <b>Show</b> toggle to disable any social network from the list</br>2) Log out by admin account</br>3) Log in by user account</br>4) Check if the disabled sharing social network is not visible for the site user|1)  Toggle changed to <b>Hide</b></br>4)  The disabled social network is not available.|

### **#4. Verify that admin can enable sharing social network links for the site users in the Share tab by Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Share</b> tab</br>- Some social networks are disabled|1) Click <b>Hide</b> toggle to enable disabled social network from the list</br>2) Log out from admin account</br>3) Log in by user account</br>4) Check if the enabled social network is visible for a site user|1)  Toggle changed to <b>Show</b></br>4)  The enabled social network is available for sharing.|

### **#5. Verify that admin can hide the Share section by click on the Show section toggle on the Share tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Share</b> tab</br>- <b>Show section</b> toggle is active|1) Click the <b>Show section</b> toggle</br>2) Log out from admin account</br>3) Log in by user account</br>4) Check if the <b>Share</b> section is present|1)Toggle changed to <b>Hide section</b></br>4) The Share section is not visible for the users|

### **#6. Verify that admin can unhide the Share section by click on the Hide section toggle on the Share tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Social Networks</b> configuration page -> <b>Share</b> tab</br>- <b>Hide section</b> toggle is shown|1) Click the <b>Hide section</b> toggle</br>2) Log out from admin account</br>3) Log in by user account</br>4) Check if the <b>Share</b> section is present|1) Toggle changed to <b>Show section</b></br>4) The <b>Share</b> section is visible for the users|

</details>
