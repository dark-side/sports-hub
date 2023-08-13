### Back to [User management on the portal](../../README.md) feature

# Allow admin user to delete users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete users
    So that they do not have an account to log in to the system

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes the user</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the users/admins list
  And I select a user and then click <b>Delete</b>
Then I see the confirmation dialog

When I click <b>Delete</b>
Then I see the confirmation dialog is closed
  And I see a notification message that the user has been OR has not been deleted
  And I see deleted user does not show up on the list
  And the message about action is sent to the user’s email
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the user management page with actions dropdown
2. Admin user sees delete confirmation pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the user management page with actions dropdown:**

![Admin user sees the user management page with actions dropdown](/sports_hub_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown_for_active_user.png)

**2. Admin user sees delete confirmation pop-up window:**

![Admin user sees delete confirmation pop-up window](/sports_hub_portal/web_application_features/site_languages/images/admin_delete_confirmation.png)

</details>

## Test cases

1. Verify that admin can delete active users on the <b>Users</b> page
2. Verify that admin can delete blocked users on the <b>Users</b> page
3. Verify that admin can delete active admin on the <b>Users</b> page
4. Verify that admin is not able to delete himself on the <b>Users</b> page
5. Verify that admin can cancel deleting users on the <b>Users</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can delete active users on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is an active user on the <b>Users</b> tab|1) For an active user, in the <b>Actions column</b>, click <b>Delete</b></br>2) On the confirmation dialog, click <b>Delete</b></br>3) Log out of admin account</br>4) Log in as a deleted user|2) The confirmation dialog appears</br>3) The user is removed from the list</br>4) The deleted user cannot log in|

### **#2. Verify that admin can delete blocked users on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a blocked user on the <b>Users</b> tab|1) For a blocked user, in the <b>Actions column</b>, click <b>Delete</b></br>2) On the confirmation dialog, click <b>Delete</b></br>3) Log out of admin account</br>4) Log in as a deleted user|2) The confirmation dialog appears</br>3) The user is removed from the list</br>4) The deleted user cannot log in|

### **#3. Verify that admin can delete active admin on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is another active admin on the <b>Admins</b> tab|1) Select the <b>Admins</b> tab</br>2) For another active admin, in the <b>Actions</b> column, click <b>Delete</b></br>3) On the confirmation dialog, click <b>Delete</b></br>4) Log out of admin account</br>5) Log in as a deleted admin|3) The confirmation dialog appears</br>4) The admin is removed from the list</br>6) The deleted admin cannot log in|

### **#4. Verify that admin is not able to delete himself on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>|1) Select the <b>Admins</b> tab</br>2) For the current admin, in the <b>Actions</b> column, click <b>Delete</b></br>3) On the confirmation dialog, click <b>Delete</b>|3) Warning message appears about no possibility to delete the currently logged-in user|

### **#5. Verify that admin can cancel deleting users on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>|1) For any admin, in the <b>Actions</b> column, click <b>Delete</b></br>2) On the confirmation dialog, click <b>Cancel</b></br>3) Log out of admin account</br>4) Log in as a user|2) The confirmation dialog appears</br>3) The user is not removed from the list</br>5) The user can log in|
</details>
