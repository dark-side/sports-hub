### Back to [User management on the portal](../../README.md) feature

# Allow admin user to remove admin permissions from users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to remove admin permissions from users

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user removes admin permissions from users</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Admins</b> tab
  And I select <b>Remove from Admin</b> on the right of any user
Then I see a confirmation dialog

When I click <b>Continue</b>
Then I see the dialog is closed
  And I see a notification message that admin permissions are OR not removed from the user
  And notification about removed admin permissions is sent to the user’s email
  And I see the user on the <b>Users</b> tab if the action was successful
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Remove from Admin</b> button within actions dropdown against admin users

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Remove from Admin button within actions dropdown against admin users:**

![Admin user sees the Remove from Admin button within actions dropdown against admin users](/desktop_application_features/user_management/images/admin_user_management_action_dropdown.png)

</details>

## Test cases

1. Verify that admin can remove admin permissions for another admin on the <b>Users</b> page
2. Verify that admin can cancel removing admin permissions for another admin on the <b>Users</b> page
3. Verify that admins are not able to remove admin permissions for themselves on the <b>Users</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can remove admin permissions for another admin on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is another admin on the <b>Admins</b> tab|1) Select the <b>Admins</b> tab</br>2) On the right of another admin, select <b>Remove from Admin</b></br>3) On the confirmation dialog, click <b>Continue</b></br>4) Log out of admin account</br>5) Log in as an another admin</br>6) Go through site pages|2) The confirmation dialog appears</br>3) Admin is set with user permissions. Notification about removed admin permissions is sent to the user’s email</br>5) The admin can log in</br>6) Another admin cannot see the admin part of the application|

### **#2. Verify that admin can cancel removing admin permissions for another admin on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is another admin on the <b>Admins</b> tab|1) Select the <b>Admins</b> tab</br>2) On the right of another admin, select <b>Remove from Admin</b></br>3) On the confirmation dialog, click <b>Cancel</b></br>4) Log out of admin account</br>5) Log in as an another admin</br>6) Go through site pages|2) The confirmation dialog appears</br>3) The admin keeps admin permissions</br>5) The user can log in</br>6) Another admin can see the admin part of application and perform actions there|

### **#3. Verify that admins are not able to remove admin permissions for themselves on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) Select the <b>Admins</b> tab</br>2) On the right of another admin, select <b>Remove from Admin</b></br>|2) The warning dialog appears about no possibility to remove admin permissions for the currently logged-in user|
</details>
