### Back to [User Management on the portal](../../) feature

# Allow admin user to search users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to have the ability to search users by name

## Acceptance criteria

    Scenario: An admin user filters the users
    Given I am logged in as an admin user
	
    When I am on the User Management page
      And I view the Users list
    Then I see a search icon with placeholder “Type a user name here”
    When I enter user’s name
    Then I see a users that match the search

## Mockups

1. Admin user sees user management page with search input field

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page with search input field:**

![User management page with search input field](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_search_input_field.png)

</details>

## Test Scenarios

1. Verify that admin can search users

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can search users**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Type the name of user in search icon with placeholder “Type a user name here”|The system displays users that match the search

</details>
