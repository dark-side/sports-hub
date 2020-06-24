### Back to [User Management on the portal](../../) feature

# Allow admin user to remove admin permissions from the user on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to remove admin permissions from the users

## Acceptance criteria

    Scenario: An admin user removes admin permissions from the user
    Given I am logged in as an admin user
	
    When I am on the User Management page
      And I view the Admins list
      And I click Remove from Admin a specific user
    Then I see a confirmation popup
    When I click Continue anyway
    Then I see a popup is closed
      And I see the system shows a notification message that admin permissions are or not removed from the user
      And I see the user in Users list if the action was successful

## Mockups

1. Admin user sees management page for admin users

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees management page for admin users:**

![Management page for admin users](/products/sport_news_portal/web_application_features/user_management/images/admin_user_management_page.png)

</details>

## Test Scenarios

1. Verify that admin is able to remove user from admin on Management page
2. Verify that admin is able to cancel action of removing user from admin on Management page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin is able to remove user from admin on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according admin users|Actions available for admins: admin users - Remove from Admin, Delete 
|6|Click on remove user from admin|A confirmation popup is shown
|7|Click on Continue anyway|The popup is closed and the system shows a notification message that the user has been deleted

### **#2. Verify that admin is able to cancel action of removing user from admin on Management page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Check the available actions for admin according admin users|Actions available for admins: admin users - Remove from Admin, Delete
|6|Click on remove user from admin|A confirmation popup is shown
|7|Click on Cancel|The popup is closed and the user is still having admin permissions

</details>
