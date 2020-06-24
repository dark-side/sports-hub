### Back to [User Management on the portal](../../) feature

# Allow admin user to delete users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to delete users
    So that they have not an account to log in to the system

## Acceptance criteria

    Scenario: A admin user deletes the user
    Given I am logged in as an admin user

    When I am on the User Management page
      And I view Users/Admins list
      And I click Delete specific user
    Then I see a confirmation popup
    When I click Delete anyway
    Then I see a popup is closed
      And I see a notification message that the user has been OR has not been deleted
      And I see deleted user does not show up in the list

## Mockups

1. Admin user sees user management page with actions dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page with actions dropdown:**

![User management page with actions dropdown](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown.png)

</details>

## Test Scenarios

1. Verify that admin is able to delete active user on Management page
2. Verify that admin is able to cancel deleting action of an active user on Management page
3. Verify that admin is able to delete blocked user on Management page
4. Verify that admin is able to cancel deleting action of blocked user on Management page
5. Verify that admin is able to delete admin user on Management page
6. Verify that admin is able to cancel deleting action of admin user on Management page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin is able to delete active user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according active users|Actions available for admins: active users - Block, Make as Admin, Delete
|6|Click to Delete active user|A confirmation popup is shown
|7|Click on delete anyway|The popup is closed and the system shows a notification message that the user has been deleted
|8|Check if deleted user is not shown in the list|Deleted user does not show up in the list

### **#2. Verify that admin is able to cancel deleting action of an active user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according active users|Actions available for admins: active users - Block, Make as Admin, Delete
|6|Click to Delete active user|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user is not deleted

### **#3. Verify that admin is able to delete blocked user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according blocked users|Actions available for admins: blocked users - Activate, Delete
|6|Click to Delete active user|A confirmation popup is shown
|7|Click on delete anyway|The popup is closed and the system shows a notification message that the user has been deleted
|8|Check if deleted user is not shown in the list|Deleted user does not show up in the list

### **#4. Verify that admin is able to cancel deleting action of blocked user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according blocked users|Actions available for admins: blocked users - Activate, Delete 
|6|Click to Delete active users|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user is not deleted

### **#5. Verify that admin is able to delete admin user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according blocked users|Actions available for admins: admin users - Remove from Admin, Delete
|6|Click to Delete admin user|A confirmation popup is shown
|7|Click on delete anyway|The popup is closed and the system shows a notification message that the user has been deleted
|8|Check if deleted user is not shown in the list|Deleted user does not show up in the list

### **#6. Verify that admin is able to cancel deleting action of admin user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according blocked users|Actions available for admins: admin users - Remove from Admin, Delete 
|6|Click to Delete active user|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user is not deleted

</details>
