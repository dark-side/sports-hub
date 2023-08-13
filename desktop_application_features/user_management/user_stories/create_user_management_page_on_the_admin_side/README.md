### Back to [User management on the portal](../../README.md) feature

# Allow admin user to view user management page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have a place with the list of users
    So that I can review and manage them

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user visits Users configuration page and have a place with the list of users</i></b>

Given I am logged in as an admin user

When I view the page
Then I see the <b>Users</b> management menu item on the left sidebar menu

When I visit the <b>Users</b> page
Then I see two tabs: Users and Admins
  And I see the list contains the user’s profile picture, name and last name, status (Active/Blocked), and actions:
    - Active: block, make as admin, delete
    - Blocked: activate, delete
    - Admin users: remove from admin, delete

<i>You have two options to render a big list: use pagination or infinite scroll</i>

</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees user management page
2. Admin user sees management page for admin users
3. Admin user sees actions dropdown against admin user

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees user management page:**

![Admin user sees user management page](/desktop_application_features/user_management/images/user_management_page.png)

**2. Admin user sees management page for admin users:**

![Admin user sees management page for admin users](/desktop_application_features/user_management/images/admin_user_management_page.png)

**3. Admin user sees actions dropdown against admin user:**

![Admin user sees actions dropdown against admin user](/desktop_application_features/user_management/images/admin_user_management_action_dropdown.png)

</details>

## Test cases

1. Verify the lists of users on the <b>Users</b> page
2. Verify the content of <b>Users</b> tab on the <b>Users</b> page
3. Verify the content of <b>Admins</b> tab on the <b>Users</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the lists of users on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) Examine the tabs on the page|1) There are two tabs: <b>Users</b> and <b>Admins</b>. The <b>Users</b> tab is active by default|

### **#2. Verify the content of Users tab on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) Examine the content of <b>Users</b> tab|1) There is a table with 3 columns: Name, Status and Actions|

### **#3. Verify the content of Admins tab on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) Select <b>Admins</b> tab</br>2) Examine the content of the <b>Admins</b> tab|2) There is a table with 3 columns: Name, Status, and Actions|
</details>
