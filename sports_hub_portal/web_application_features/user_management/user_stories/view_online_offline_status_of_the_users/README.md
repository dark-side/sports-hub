### Back to [User management on the portal](../../) feature

# Allow admin user to view online/offline status of users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to see if users are online/offline

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views online/offline users</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> or <b>Admins</b> tab
Then I see a green status dot if users have an active session on the site
  And I see the system displays a gray status dot if users do not have an active session on the site
</pre>

## Mockups

1. Admin user sees users being online/offline

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees users being online/offline:**

![Admin user sees users being online/offline](/products/sports_hub_portal/web_application_features/user_management/images/user_management_page.png)

</details>

## Test cases

1. Verify that admin can see online status of users
2. Verify that admin can see offline status of users

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can see online status of users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There are users with active sessions|1) Check if the status of the active users is shown as a green status dot|1) The system displays a green status dot if users have an active session on the site|

### **#2. Verify that admin can see offline status of users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There are users with inactive sessions|1) Check if the status of the not active users is shown as a gray status dot|1) The system displays a gray status dot if users do not have an active session on the site|
</details>
