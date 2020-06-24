### Back to [User Management on the portal](/../../) feature

# Allow admin user to activate users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to activate users
    So that they will have access to comments

## Acceptance criteria

    Scenario: An admin user activates the user
    Given I am logged in as an admin user

    When I am on the User Management page
      And I view Users list
    Then I see a Activate action against blocked users
    When I click Activate specific user
    Then I see a confirmation popup
    When I click Continue anyway
    Then I see a popup is closed
      And I see the notification message that the user has been OR has not been activated
      And I see the user’s status is changed to Active if the action was successful
      And I see the activated user do not have the ability to view the comments and comment

## Mockups

1. Admin user sees user management page with actions dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page with actions dropdown:**

![User management page with actions dropdown](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown.png)

</details>

## Test Scenarios

1. Verify that admin is able to activate blocked user on Management page
2. Verify that admin is able to cancel activating action of blocked user on Management page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin is able to activate blocked user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for blocked users|Actions available for admins: blocked users - Activate, Delete
|6|Click on Activate blocked user|A confirmation popup is shown
|7|Click on Continue anyway|The popup is closed and the system shows a notification message that the user has been blocked

### **#2. Verify that admin is able to cancel activating action of blocked user on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according blocked users|Actions available for admins: blocked users - Block, Make as Admin, Delete 
|6|Click on activate blocked user|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user is still blocked

</details>
