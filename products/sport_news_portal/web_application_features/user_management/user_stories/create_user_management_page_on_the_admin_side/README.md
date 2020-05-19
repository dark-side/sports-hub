### Back to [User Management on the portal](/../../) feature

# Allow admin user to view User Management page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have a place with the list of users
    So that I can review and manage them

## Acceptance criteria

    Scenario: An admin user visits User Management page and have a place with the list of users
    Given I am logged in as an admin user

    When I view the page
    Then I see a User Management menu item on the left sidebar
    When I visit User Management page
    Then I see a two lists: Users and Admin Users
      And I see the list contains the user’s avatar, name and last name, status (Active/Blocked), and actions:
      -  Active users - Block, Make as Admin, Delete
      -  Blocked users - Activate, Delete
      -  Admin users - Remove from Admin, Delete

## Mockups

1. Admin user sees user management page
2. Admin user sees management page for admin users

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page:**

![User management page](/products/sport_news_portal/web_application_features/user_management/images/user_management_page.png)

**2. Admin user sees management page for admin users:**

![Management page for admin users](/products/sport_news_portal/web_application_features/user_management/images/admin_user_management_page.png)

</details>

## Test Scenarios

1. Verify that admin can view user Management item
2. Verify that user cannot view user Management item
3. Verify the lists of user Management page
4. Verify the content of the lists of user Management page
5. Verify the actions of the user Management page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can view user Management item**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|User Management menu item is situated on the left sidebar

### **#2. Verify that user cannot view user Management item**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Observe User Management menu item|User Management menu item is not shown for users

### **#3. Verify the lists of user Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check what lists contain the User Management page|The system shows two lists: Users and Admin Users on the Management page

### **#4. Verify the content of the lists of user Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the content of the lists of user Management page|List contains the user’s avatar, name and last name, status (Active/Blocked), and actions

### **#5. Verify the actions of the user Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the content of the lists of user Management page|List contains the user’s avatar, name and last name, status (Active/Blocked), and actions
|6|Check what actions are available for admin|Actions available for admins:<br> - active users - Block, Make as Admin, Delete<br> - blocked users - Activate, Delete<br> - admin users - Remove from Admin, Delete

</details>
