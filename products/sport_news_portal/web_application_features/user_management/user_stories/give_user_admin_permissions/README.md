### Back to [User management on the portal](../../) feature

# Allow admin user to give user admin permissions on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to give active users admin permissions

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user makes the user as admin</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
And I view the <b>Users</b> tab

And I select any active user, and then I select <b>Make as Admin</b>
Then I see a confirmation dialog

When I click <b>Continue</b>
Then I see the dialog is closed
  And I see a notification message that the user has got OR has not got admin permissions
  And notification about admin permissions is sent to the user’s email
  And I see the user on the <b>Admins</b> tab if the action was successful
</pre>

## Mockups

1. Admin user sees Make as Admin button within actions dropdown against active user

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Make as Admin button within actions dropdown against active user:**

![Admin user sees Make as Admin button within actions dropdown against active user](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown_for_active_user.png)

</details>

## Test cases

1. Verify that admin can set admin permissions for an active user on the Users page
2. Verify that admin can cancel setting admin permissions for active user on the Users page
3. Verify that admin is not able to set admin permissions for a blocked user on the Users page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can set admin permissions for an active user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There is an active user on the <b>Users</b> tab|1) On the right of any active user, select the <b>Make as Admin</b> action</br>2) On the confirmation dialog, click <b>Continue</b></br>3) Log out as admin user</br>4) Login as changed user</br>5) Go through admin pages|1) The confirmation dialog appears</br>2) The user is set with admin permissions. Notification about admin permissions is sent to the user’s email</br>4) The user can log in</br>5) Can see administration part of the application and perform actions there|

### **#2. Verify that admin can cancel setting admin permissions for active user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There is an active user on the <b>Users</b> tab|1) On the right of any active user, select the <b>Make as Admin</b> action</br>2) On the confirmation dialog, click <b>Cancel</b></br>3) Log out as admin user</br>4) Login as changed user</br>5) Go through site pages|1) The confirmation dialog appears</br>2) The user has only user permissions</br>4) The user can log in</br>5) The user cannot see the administration part of the application|

### **#3. Verify that admin is not able to set admin permissions for a blocked user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a blocked user on the <b>Users</b> tab|1) On the right of any blocked user, click the actions drop-down button group|1) There is no <b>Make as Admin</b> action|


</details>
