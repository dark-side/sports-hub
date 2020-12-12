### Back to [User Management on the portal](../../) feature

# Allow admin user to view online/offline status of the user on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to see if users are online/offline

## Acceptance criteria

<pre>
Scenario: An admin user views online/offline users
Given I’m logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> or <b>Admins</b> tab
Then I see a green status dot if users have an active session on the site
  And I see the system displays a gray status dot if users do not have an active session on the site
</pre>

## Mockups

1. Admin user sees users being online/ofline

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees users being online/ofline:**

![Admin user sees users being online/ofline](/products/sport_news_portal/web_application_features/user_management/images/user_management_page.png)

</details>

## Test cases

1. Verify that admin can view online status of the users
2. Verify that admin can view offline status of the users

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can view online status of the users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There are users with active sessions|1) Check if the status of the active users is shown as a green status dot|1) The system displays a green status dot if users have an active session on the site|

### **#2. Verify that admin can view offline status of the users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There are users with inactive sessions|1) Check if the status of the not active users is shown as a gray status dot|1) The system displays a gray status dot if users have an active session on the site|
</details>
