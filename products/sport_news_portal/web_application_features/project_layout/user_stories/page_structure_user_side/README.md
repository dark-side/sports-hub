### Back to [Page layout on the portal](../../) feature

# Page Structure

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
Then I see the page consists of:
  - Header section that is common for all pages, includes:
    1. Social network icons (configured by the admin)
    2. Global search box
    3. Sport News logo
    4. Sign up and Log in buttons (in case user is not logged in) 
    5. User name, Profile picture, and profile link (in case user is logged in)
    6. Site language drop-down menu (language list is configured by the admin)
  - Main navigation sidebar menu on the left that is common to all pages
  - The main content area with content blocks, configured by the admin
  - Right sidebar with content blocks, configured by the admin 
  - Footer section that is common to all pages, configured by the admin

When I click on the <b>Sport News</b> logo
Then I am taken to the Sport News home page 
  And I see the <b>Home</b> menu item is active

When I click on a link to an external site 
Then I see the site is opened on a new browser tab

</pre>

## Mockups

1. User sees Home page structure when user is signed-in
2. User sees Home page structure when user is not signed-in

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Home page structure when user is signed-in:**

![User sees Home page structure when user is signed-in](/products/sport_news_portal/web_application_features/project_layout/images/home_page_logged_in_user.png)

**2. User sees Home page structure when user is not signed-in:**

![User sees Home page structure when user is not signed-in](/products/sport_news_portal/web_application_features/project_layout/images/home_page_logged_out_user.png)

</details>

## Test cases

1. Verify that the link to an external site is opened in a separate browser tab
2. Verify that the user is able to navigate to the home page by clicking on the logo

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the link to an external site is opened in a separate browser tab**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to Sport News home page|1) Go to any page</br>2) Сlick on a link to an external site|2) The site opens on a new browser tab|

### **#2. Verify that the user is able to navigate to the home page by clicking on the logo**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to Sport News home page|1) Go to any page</br>2) In the upper-left corner of the page, click on the logo|2) User goes to the home page|

</details>
