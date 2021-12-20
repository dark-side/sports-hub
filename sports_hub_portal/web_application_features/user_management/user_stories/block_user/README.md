### Back to [User management on the portal](../../) feature

# Allow admin user to block users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to block users
    So that they won’t have access to comments

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user blocks the user</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> tab
Then I see the <b>Block</b> button on the right of active users

When I select an active user and then click <b>Block</b>
Then I see the confirmation dialog

When I click <b>Continue</b>
Then I see the confirmation dialog is closed
  And I see a notification message that the user has been OR has not been blocked
  And I see the user’s status is changed to <b>Blocked</b> if the action was successful
  And the blocked user cannot comment
  And notification about blocking is sent to the user’s email
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions dropdown against active user
2. Admin user sees warning pop-up window on the user block

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions dropdown against active user:**

![Admin user sees actions dropdown against active user](/sports_hub_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown_for_active_user.png)

**2. Admin user sees warning pop-up window on the user block:**

![Admin user sees warning pop-up window on the user block](/sports_hub_portal/web_application_features/user_management/images/before_user_block_warning_popup.png)

</details>

## Test cases

1. Verify that admin can block an active user on the <b>Users</b> page
2. Verify that admin can cancel blocking an active user on the <b>Users</b> page
3. Verify that admin is not able to block admin on the <b>Users</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can block an active user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is an active user on the <b>Users</b> tab|1) On the right of an active user, click <b>Block</b></br>2) On the confirmation dialog, click <b>Continue</b></br>3) Log out of admin account</br>4) Log in as a blocked user</br>5) Go through pages with comments|1) The confirmation dialog appears</br>2) The user has a <b>Blocked</b> state. Notification about blocking is sent to the user’s email</br>4) The user can log in</br>5) The user cannot write comments|

### **#2. Verify that admin can cancel blocking an active user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is an active user on the <b>Users</b> tab|1) On the right of an active user, click <b>Block</b></br>2) On the confirmation dialog, click <b>Cancel</b></br>3) Log out of admin account</br>4) Log in as a user</br>5) Go through pages with comments|1) The confirmation dialog appears</br>2) The user has the <b>Active</b> state</br>4) The user can log in</br>5) The user can see and write comments|

### **#3. Verify that admin is not able to block admin on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is another active admin on the <b>Admins</b> tab|1) Select the <b>Admins</b> tab</br>2) On the right of another admin, click the actions drop-down button group|2) There is no <b>Block</b> action|

</details>
