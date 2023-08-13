### Back to [User management on the portal](../../README.md) feature

# Allow admin user to activate users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to activate users
    So that they will have access to comments

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user activates the user</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> tab
Then I see the <b>Activate</b> action next to a blocked user

When I click <b>Activate</b>
Then I see the confirmation dialog

When I click <b>Continue</b>
Then I see the dialog is closed
  And I see a notification message that the user has been OR has not been activated
  And I see the user’s status is changed to <b>Active</b> if the action was successful
  And I see the activated user can view the comments and comment
  And notification about activation is sent to the user’s email
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions dropdown against blocked users

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions dropdown against blocked users:**

![Admin user sees actions dropdown against blocked users](/sports_hub_portal/desktop_application_features/user_management/images/user_management_page_with_action_dropdown_for_blocked_user.png)

</details>

## Test cases

1. Verify that admin can activate blocked users on the <b>Users</b> page
2. Verify that admin can cancel activating blocked users on the <b>Users</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can activate blocked users on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a blocked user on the <b>Users</b> tab|1) On the right of an active user, click the <b>Activate</b> action</br>2) On the confirmation dialog, click <b>Continue</b></br>3) Log out of admin account</br>4) Log in as an activated user</br>5) Go through pages with comments|1) The confirmation dialog appears</br>2) The user has the <b>Active</b> state. Notification about activation is sent to the user’s email</br>4) The user can log in</br>5) The user can see and write comments|

### **#2. Verify that admin can cancel activating blocked users on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a blocked user on the <b>Users</b> tab|1) On the right of an active user, click the <b>Activate</b> action</br>2) On the confirmation dialog, click <b>Cancel</b></br>3) Log out of admin account</br>4) Log in as an activated user</br>5) Go through pages with comments|1) The confirmation dialog appears</br>2) The user stays in <b>Blocked</b> state</br>4) The user can log in</br>5) The user cannot write comments|
</details>
