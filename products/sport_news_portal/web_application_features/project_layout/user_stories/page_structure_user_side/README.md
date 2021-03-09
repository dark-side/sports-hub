### Back to [Page layout on the portal](../../) feature

# Page structure (user side)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view the same layout structure across all the pages

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views layout structure across all the pages</i></b>

Given I am a site user

When I view any page on the site
Then I see the page consisting of:
  - Header section that is common for all pages includes:
    1. Social network icons (configured by admin)
    2. Global search box
    3. Sports Hub logo
    4. <b>Sign up</b> and <b>Log in</b> buttons (in case user is not logged in) 
    5. User name, Profile picture, and profile link (in case user is logged in)
    6. Site language drop-down menu (language list is configured by admin)
  - Main navigation sidebar menu on the left that is common to all pages
  - The main content area with content blocks, configured by admin
  - Right sidebar with content blocks, configured by admin 
  - Footer section that is common to all pages, configured by admin

When I select the <b>Sports Hub</b> logo
Then I am taken to the Sports Hub home page
  And I see the <b>Home</b> menu item is active

When I select a link to an external site 
Then I see the site opens in a new browser tab

</pre>

## Mockups

1. Users see <b>Home</b> page structure when they are signed in
2. Users see <b>Home</b> page structure when they are not signed in

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Home page structure when they are signed in:**

![Users see Home page structure when they are signed in](/products/sport_news_portal/web_application_features/project_layout/images/home_page_logged_in_user.png)

**2. Users see Home page structure when they are not signed in:**

![Users see Home page structure when they are not signed in](/products/sport_news_portal/web_application_features/project_layout/images/home_page_logged_out_user.png)

</details>

## Test cases

1. Verify that the link to an external site is opened in a separate browser tab
2. Verify that the user is able to navigate to the <b>Home</b> page by selecting the logo

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the link to an external site is opened in a separate browser tab**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to the Sports Hub home page|1) Go to any page</br>2) Select a link to an external site|2) The site opens in a new browser tab|

### **#2. Verify that the user is able to navigate to the Home page by selecting the logo**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to the Sports Hub home page|1) Go to any page</br>2) In the upper-left corner of the page, select the logo|2) The user goes to the home page|

</details>
