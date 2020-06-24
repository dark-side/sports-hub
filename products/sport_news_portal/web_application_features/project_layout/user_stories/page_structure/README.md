### Back to [Page Layout on the portal](../../) feature

# Page Structure

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to view same layout structure across all the pages

## Acceptance criteria

    Scenario: As a site user views layout structure across all the pages
    Given I am logged in as a site user

    When I view any page on the site
    Then I see page consisting of:
      - Header Section that is common to all pages, includes:
          - Social sharing icons (configured by the admin)
          - Global search input
          - Sport News logo
          - Sign up and Log in buttons (in case user is not logged in)
          - User name, avatar and profile link (in case user is logged in)
          - Site language dropdown (language list is configured by the admin)
      - Main navigation menu in the left sidebar that is common to all page
      - The main content area made of up blocks of content, configured by the admin
      - right sidebar content made of up blocks of content, configured by the admin
      - footer section that is common to all pages, configured by the admin
    When I click on the Sport News logo
    Then I am taken to the Sport News Home page
        And I see the Home menu item is active
    When I click on a link to an external site
    Then I see the site is opened in a separate browser tab

## Mockups

1. User sees Home page structure when user is signed-in
2. User sees Home page structure when user is not signed-in

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Home page structure when user is signed-in:**

![Home page when user is signed-in Screen](/products/sport_news_portal/web_application_features/project_layout/images/home_page_when_user_is_loged_in.png)

**2. User sees Home page structure when user is not signed-in:**

![Home page when user is not signed-in Screen](/products/sport_news_portal/web_application_features/project_layout/images/home_page_when_user_is_not_loged_in.png)

</details>

## Test Scenarios

1. Verify presence of main sections of any page of the site
2. Verify components of the Header section
3. Verify content area blocks
4. Verify that footer section is common for all pages

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify presence of main sections of any page of the site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in to user account|
|3|Observe main sections of any page of the site|Every page consists of:<br>- Header section<br> - Main navigation menu in the left side bar<br> - The main content area<br>- Sidebar content<br>- Footer section

### **#2. Verify components of the Header section**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in to user account|
|3|Observer header section|A Header section is at the top of the page
|4|Examine what components the header section consists of|The Header section consists of:<br>- Social sharing icons (configured by the admin)<br>- Global search input<br>- Sport News logo<br>- Sign up and Log in buttons (in case user is not logged in) <br>- User name, avatar and profile link (in case user is logged in)<br>- Site language dropdown (language list is configured by the admin)

### **#3. Verify content area blocks**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Observe content area blocks|The main content area made of up blocks of content, configured by the admin

### **#4. Verify that footer section is common for all pages**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Navigate from page to page and observe the footer section|Footer Section is common to all page

</details>
