### Back to [Page Layout on the portal](../../) feature

# Page Structure

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the administration office

## Acceptance criteria

<pre>
Scenario: An admin user views the administration office
Given I am logged in as an admin user

When I view the administration office
Then I see the page consisting of:
  - Header section that includes:
    1. Sport News logo
    2. Switch to user view button, user name, profile picture, and profile link
    3. Active configuration page name
    4. Horizontal menu with static items (Home (active by default), Lifestyle, Video, Dealbook) and created ones
  - Left vertical menu to configure Surveys, Banners, Languages, Footer, Social Networks, Users, Information architecture (sports categories, subcategories (conferences), teams), Teams, News Partners, Advertising. 

  - The main admin work area
  - Right sidebar content with blocks of content, configured by the admin 
  - Footer section that is common to all pages, configured by the admin

When I hover over items on the left vertical menu
Then I see their names

When I click the <b>Switch to user view</b> button
Then button changes to the <b>Switch to admin view</b>
  And I am taken to the user side of Sport News home page where I can act as a regular user

When I click the <b>Switch to admin view</b> button
Then button changes to the <b>Switch to user view</b>
  And I am taken to the admin side of Sport News home page where I can act as an admin

</pre>

## Mockups

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin sees administration side:**

![Admin sees administration side](/products/sport_news_portal/web_application_features/project_layout/images/admin_side.png)

</details>

## Test cases

1. Verify that the admin is able to act as a user by click Switch to user view button
2. Verify that the admin is able to go back to admin view by click Switch to admin view button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the admin is able to act as a user by click Switch to user view button**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- Log in by admin account|1) Go to any page</br>2) Click on the **Switch to user view** button in the upper-right corner of the page</br>3) Browse different pages|2) Admin goes to the home page in user view mode</br>3) Admin can interact with pages as a regular user|

### **#2. Verify that the admin is able to go back to admin view by click Switch to admin view button**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Admin in a user view mode|1) Go to any page</br>2) Click on the **Switch to admin view** button in the upper-right corner of the page</br>3) Browse different pages|2) Admin goes to the home page in admin mode</br>3) Admin can interact with pages as an admin|

</details>
