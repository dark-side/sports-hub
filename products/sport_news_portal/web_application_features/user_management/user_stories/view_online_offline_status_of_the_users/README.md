### Back to [User Management on the portal](/../../) feature

# Allow admin user to view online/offline status of the user on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to see if users are online/offline

## Acceptance criteria

    Scenario: An admin user views online/offline users
    Given I am logged in as an admin user
	
    When I am on the User Management page
      And I view the Users/Admins list
    Then I see a green circle if users have an active session on the site
      And I see the system displays a gray circle if users do not have a session on the site
    
## Mockups

1. Admin user sees user management page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page:**

![User management page](/products/sport_news_portal/web_application_features/user_management/images/user_management_page.png)

</details>

## Test Scenarios

1. Verify that admin is able to view online status of the users
2. Verify that admin is able to view offline status of the users

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin is able to view online status of the users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Observe the Users/Admins list|
|6|Check if the status of the user is shown as a green cycle|The system displays a green circle if users have an active session on the site

### **#2. Verify that admin is able to view offline status of the users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Observe User Management menu item|
|4|Go to User Management page|
|5|Observe the Users/Admins list|
|6|Check if the status of the user is shown as a gray cycle|The system displays a gray circle if users have an active session on the site

</details>
