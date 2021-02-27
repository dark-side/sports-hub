### Back to [Page layout on the portal](../../) feature

# Page structure (admin side)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the administration office

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the administration office</i></b>

Given I am logged in as an admin user

When I view the administration office
Then I see the page consisting of:
  - Header section that includes:
    1. Sports Hub logo
    2. <b>Switch to user view</b> button, user name, profile picture, and profile link
    3. Active configuration page name
    4. Horizontal menu with static items (Home (active by default), Lifestyle, Video, Dealbook) and created ones
  - Left vertical menu to configure Surveys, Banners, Languages, Footer, Social Networks, Users, Information architecture (sports categories, subcategories (conferences), teams), Teams, News Partners, Advertising. 

  - The main admin work area
  - Right sidebar content with blocks of content, configured by admin
  - Footer section that is common to all pages, configured by admin

When I hover over items on the left vertical menu
Then I see their names

When I click the <b>Switch to user view</b> button
Then button changes to the <b>Switch to admin view</b>
  And I am taken to the user side of Sports Hub home page where I can act as a regular user

When I click the <b>Switch to admin view</b> button
Then button changes to the <b>Switch to user view</b>
  And I am taken to the admin side of Sports Hub home page where I can act as an admin
</pre>

## Mockups

1. Admin user sees administration side

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees administration side:**

![Admin user sees administration side](/products/sport_news_portal/web_application_features/project_layout/images/admin_side.png)

</details>

## Test cases

1. Verify that admin is able to act as a user by clicking <b>Switch to user view</b>
2. Verify that admin is able to go back to admin view by clicking <b>Switch to admin view</b>

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to act as a user by clicking Switch to user view**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Log in with admin account|1) Go to any page</br>2) Click **Switch to user view** in the upper-right corner of the page</br>3) Browse different pages|2) Admin goes to the home page in the user view mode</br>3) Admin can interact with pages as a regular user|

### **#2. Verify that admin is able to go back to admin view by clicking Switch to admin view**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Log in with admin account</br>- Admin in the user view mode|1) Go to any page</br>2) Click **Switch to admin view** in the upper-right corner of the page</br>3) Browse different pages|2) Admin goes to the home page in admin mode</br>3) Admin can interact with pages as an admin|

</details>
