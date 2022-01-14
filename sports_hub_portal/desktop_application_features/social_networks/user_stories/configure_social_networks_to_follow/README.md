### Back to [Social networks on the portal](../../) feature

# Allow admin user to configure social networks for following

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure on which social networks users can follow Sports Hub

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures which social networks are to be followed</i></b>

Given I am logged in as an admin user

When I view the <b>Social networks</b> configuration page
Then I see three tabs available for configuration: <b>Share</b>, <b>Follow</b>, <b>Log in/Sign up</b>

When I click the <b>Follow</b> tab
Then I see the following:
  - <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, <b>YouTube</b> social networks list that can be used to follow the Sports Hub page on the social networks
  - <b>Show/Hide</b> toggle for each specific social network
  - <b>Show section</b> toggle
  All social networks are shown by default

When I click the <b>Show</b> toggle for any of the social networks from the list
Then the toggle changes to <b>Hide</b>
  And it is no longer shown in the navigation menu for users

When I click the <b>Hide</b> toggle for any of the social networks from the list
Then the toggle changes to <b>Show</b>
  And it is shown in the navigation menu for users

When I click the <b>Show section</b> toggle
Then the toggle changes to <b>Hide section</b>
  And the whole <b>Follow</b> section is no longer shown in the navigation menu for users

When I click the <b>Hide section</b> toggle
Then the toggle changes to <b>Show section</b>
  And the whole <b>Follow</b> section is shown on the navigation menu for users
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>Follow</b> configuration page with <b>Show section</b> on
2. Admin user sees <b>Follow</b> configuration page with <b>Show section</b> off
3. User sees <b>Follow</b> icons in the navigation menu

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Follow configuration page with Show section on:**

![Admin user sees Follow configuration page with Show section on](/sports_hub_portal/desktop_application_features/social_networks/images/following_configuration_page.png)

**2. Admin user sees Follow configuration page with Show section off:**

![Admin user sees Follow configuration page with Show section off](/sports_hub_portal/desktop_application_features/social_networks/images/following_configuration_page_section_off.png)

**3. User sees Follow icons in the site header:**

![User sees Follow icons in the navigation menu](/sports_hub_portal/desktop_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test cases

1. Verify the content of the <b>Follow</b> tab on the <b>Social networks</b> page
2. Verify that admin can disable following social network links for the site users on the <b>Follow</b> tab by <b>Show</b> toggle
3. Verify that admin can enable following social network links for the site users on the <b>Follow</b> tab by <b>Hide</b> toggle
4. Verify that admin can hide the <b>Follow</b> section by clicking the <b>Show section</b> toggle on the <b>Follow</b> tab
5. Verify that admin can unhide the <b>Follow</b> section by clicking the <b>Hide section</b> toggle on the <b>Follow</b> tab

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Follow tab on the Social networks page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page|1) Examine the content on the <b>Follow</b> tab|1) There is the social network list: <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, <b>YouTube</b>. The <b>Show/Hide</b> toggle to activate/deactivate a specific social network and the <b>Show section</b> toggle|

### **#2. Verify that admin can disable following social network links for the site users on the Follow tab by Show toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Follow</b> tab</br>- All social networks are enabled for following|1) Click the <b>Show</b> toggle for any social network from the list</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if the disabled social network is not visible to site users|1) The toggle changed to <b>Hide</b></br>4) The disabled social network is not available for following|

### **#3. Verify that admin can enable following social network links for the site users on the Follow tab by Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Follow</b> tab</br>- Some social networks are disabled for following|1) Click the <b>Hide</b> toggle for any social network from the list</br>2) Log out of admin account</br>3) Log in with user account</br>4) Examine if enabled following social network is visible to site users|1) The toggle changed to <b>Show</b></br>4) The enabled social network is available for following|

### **#4. Verify that admin can hide the Follow section by clicking the Show section toggle on the Follow tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Follow</b> tab</br>- <b>Show section</b> toggle is shown|1) Click the <b>Show section</b> toggle</br>2) Log out of admin account</br>3) Log in with user account</br>4) Examine if the <b>Follow</b> section is present|1) The toggle changed to <b>Hide section</b></br>4) The <b>Follow</b> section is not visible to users|

### **#5. Verify that admin can unhide the Follow section by clicking the Hide section toggle on the Follow tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Social networks</b> configuration page > <b>Follow</b> tab</br>- <b>Hide section</b> is shown|1) Click the <b>Hide section</b> toggle</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if the <b>Follow</b> section is present|1) The toggle changed to <b>Show section</b></br>4) The <b>Follow</b> section is visible to users|

</details>
