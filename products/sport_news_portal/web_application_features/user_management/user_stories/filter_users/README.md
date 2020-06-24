### Back to [User Management on the portal](/../../) feature

# Allow admin user to filter users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to filter users based on criteria
    So that I can perform the needed action

## Acceptance criteria

    Scenario: An admin user filters the users
    Given I am logged in as an admin user
	
    When I am on the User Management page
      And I view the Users list
    Then I see a filter with options: Active, Blocked, Online, Offline
    When I select any of the options
    Then I see a relevant result and amount of selected users

## Mockups

1. Admin user sees user management page with filter dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page with filter dropdown:**

![User management page with filter dropdown](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_filter_dropdown.png)

</details>

## Test Scenarios

1. Verify that admin can filter active users
2. Verify that admin can filter blocked users
3. Verify that admin can filter online users
4. Verify that admin can filter offline users

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can filter active users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Observe the Users/Admins list with available options|The system displays a filter with options: Active, Blocked, Online, Offline
|6|Click on Active option|The system displays all active users from the list

### **#2. Verify that admin can filter blocked users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Observe the Users/Admins list with available options|The system displays a filter with options: Active, Blocked, Online, Offline
|6|Click on blocked option|The system displays all blocked users from the list

### **#3. Verify that admin can filter online users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Observe the Users/Admins list with available options|The system displays a filter with options: Active, Blocked, Online, Offline
|6|Click on online option|The system displays all online users from the list

### **#4. Verify that admin can filter offline users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Observe the Users/Admins list with available options|The system displays a filter with options: Active, Blocked, Online, Offline
|6|Click on offline option|The system displays all offline users from the list

</details>
