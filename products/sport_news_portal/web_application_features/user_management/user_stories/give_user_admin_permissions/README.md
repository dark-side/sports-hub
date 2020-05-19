### Back to [User Management on the portal](/../../) feature

# Allow admin user to give user admin permissions on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to give users admin permissions

## Acceptance criteria

    Scenario: An admin user makes the user as admin
    Given I am logged in as an admin user
	
    When I am on the User Management page
      And I view Users list
      And I click Make as Admin a specific user
    Then I see a confirmation popup
    When I click Continue anyway
    Then I see a popup is closed
      And I see the notification message that the user has got OR has not got admin permissions
      And I see the user in Admin Users list if the action was successful

## Mockups

1. Admin user sees user management page with actions dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page with actions dropdown:**

![User management page with actions dropdown](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown.png)

</details>

## Test Scenarios

1. Verify that admin is able to give user admin permissions on Management page
2. Verify that admin is able to cancel action of giving an active user an admin permission on Management page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin is able to give user admin permissions on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according active users|Actions available for admins: active users - Block, Make as Admin, Delete
|6|Click on Make as Admin active user|A confirmation popup is shown
|7|Click on Continue anyway|The popup is closed and the system shows a notification message that the user has been given an admin permissions

### **#2. Verify that admin is able to cancel action of giving an active user an admin permission on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according active users|Actions available for admins: active users - Block, Make as Admin, Delete 
|6|Click Make as Admin active user|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user has not been given an admin permissions

</details>
