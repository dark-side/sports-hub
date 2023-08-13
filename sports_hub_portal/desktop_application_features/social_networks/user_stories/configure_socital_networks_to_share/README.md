### Back to [Social networks on the portal](../../README.md) feature

# Allow admin user to configure social networks for sharing

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure which social networks users can use to share the Sports Hub site

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures which social networks are to be shared</i></b>

Given I am logged in as an admin user

When I view the <b>Social networks</b> configuration page
Then I see three tabs available for configuration: <b>Share</b>, <b>Follow</b>, <b>Log in/Sign up</b>

When I am on the <b>Share</b> tab
Then I see the following:
  - <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b> social networks list that can be used for sharing a Sports Hub page
  - The <b>Show/Hide</b> toggle for each specific social network
  - The <b>Show section</b> toggle
  And all social networks are visible by default

When I click the <b>Show</b> toggle for any of the social networks from the list
Then the toggle changes to <b>Hide</b>
  And it is no longer shown in the header section for users

When I click the <b>Hide</b> toggle for any social networks from the list
Then the toggle changes to <b>Show</b>
  And it is visible to users in the header section

When I click the <b>Show section</b> toggle
Then the toggle changes to <b>Hide section</b>
  And the whole <b>Share</b> section is no longer visible to users in the site header

When I click the <b>Hide section</b> toggle
Then the toggle changes to <b>Show section</b>
  And the whole <b>Share</b> section is visible to users in the site header
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>Share</b> configuration page with <b>Show section</b> on
2. Admin user sees <b>Share</b> configuration page with <b>Show section</b> off
3. Users see <b>Share</b> icons in the site header

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Share configuration page with Show section on:**

![Admin user sees Share configuration page with Show section on](/sports_hub_portal/desktop_application_features/social_networks/images/sharing_configuration_page.png)

**2. Admin user sees Share configuration page with Show section off:**

![Admin user sees Share configuration page with Show section off](/sports_hub_portal/desktop_application_features/social_networks/images/sharing_configuration_page_section_off.png)

**3. Users see Share icons in the site header:**

![Users see Share icons in the site header](/sports_hub_portal/desktop_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test cases

1. Verify the tabs on the <b>Social networks</b> page
2. Verify the content of the <b>Share</b> tab on a <b>Social networks</b> page
3. Verify that admin can disable sharing social network links on the <b>Share</b> tab by the <b>Show</b> toggle
4. Verify that admin can enable sharing social network links for the site users on the <b>Share</b> tab by the <b>Hide</b> toggle
5. Verify that admin can hide the <b>Share</b> section by clicking the <b>Show</b> section toggle on the <b>Share</b> tab
6. Verify that admin can unhide the <b>Share</b> section by clicking the <b>Hide</b> section toggle on the <b>Share</b> tab

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the tabs on the Social networks page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page|1) Examine the tabs on the page|1) There are three tabs: <b>Share</b>, <b>Follow</b>, <b>Log in/Sign up</b>. The <b>Share</b> tab is active by default|

### **#2. Verify the content of the Share tab on a Social networks page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page|1) Examine the content on the <b>Share</b> tab|1) There is a social network list: <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, <b>YouTube</b>. The <b>Show/Hide</b> toggle to activate/deactivate a social network and the <b>Show section</b> toggle|

### **#3. Verify that admin can disable sharing social network links on the Share tab by the Show toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Share</b> tab|1) Click the <b>Show</b> toggle to disable any social network from the list</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if the disabled sharing social network is not visible to site users|1) The toggle changed to <b>Hide</b></br>4) The disabled social network is not available|

### **#4. Verify that admin can enable sharing social network links for the site users on the Share tab by the Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Share</b> tab</br>- Some social networks are disabled|1) Click the <b>Hide</b> toggle to enable disabled social network from the list</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if the enabled social network is visible to site users|1) The toggle changed to <b>Show</b></br>4) The enabled social network is available for sharing|

### **#5. Verify that admin can hide the Share section by clicking the Show section toggle on the Share tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Share</b> tab</br>- The <b>Show section</b> toggle is active|1) Click the <b>Show section</b> toggle</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if <b>Share</b> section is present|1) The toggle changed to <b>Hide section</b></br>4) The <b>Share</b> section is not visible to users|

### **#6. Verify that admin can unhide the Share section by clicking the Hide section toggle on the Share tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Share</b> tab</br>- The <b>Hide section</b> toggle is shown|1) Click the <b>Hide section</b> toggle</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if <b>Share</b> section is present|1) The toggle changed to <b>Show section</b></br>4) The <b>Share</b> section is visible to users|

</details>
