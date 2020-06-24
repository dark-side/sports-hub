### Back to [User Management on the portal](../../) feature

# Allow admin user to block users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to block users
    So that they won’t have access to comments

## Acceptance criteria

    Scenario: An admin user blocks the user
    Given I am logged in as an admin user
	
    When I am on the User Management page
      And I view Users list
    Then I see a Block action against active users
    When I click Block specific user
    Then I see a confirmation popup
    When I click Continue anyway
    Then I see a popup is closed
      And I see the system shows a notification message that the user has been OR has not been blocked
      And I see the user’s status is changed to Blocked if the action was successful
      And I see blocked user do not have the ability to view the comments and comment

## Mockups

1. Admin user sees user management page with actions dropdown
2. Admin user sees warning popup before user block

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page with actions dropdown:**

![User management page with actions dropdown](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown.png)

**2. Admin user sees warning popup before user block:**

![Warning popup before user block](/products/sport_news_portal/web_application_features/user_management/images/before_user_block_warning_popup.png)

</details>

## Test Scenarios

1. Verify that admin is able to block active user on Management page
2. Verify that admin is able to cancel blocking action of an active user on Management page
3. Verify that admin is not able to block admin user on Management page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin is able to block active user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according active users|Actions available for admins: active users - Block, Make as Admin, Delete
|6|Click on Block active user|A confirmation popup is shown
|7|Click on Continue anyway|The popup is closed and the system shows a notification message that the user has been blocked
|8|Check if blocked user haven’t the ability to view the comments and comment|The blocked user will not have the ability to view the comments and comment

### **#2. Verify that admin is able to cancel blocking action of an active user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according active users|Actions available for admins: active users - Block, Make as Admin, Delete 
|6|Click on Block active user|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user is not blocked

### **#3. Verify that admin is not able to block admin user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check if block action is available for admin user|Admin cannot block another admin user

</details>
