### Back to [User Management on the portal](../../) feature

# Allow admin user to activate users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to activate users
    So that they will have access to comments

## Acceptance criteria

<pre>
Scenario: An admin user activates the user
Given I’m logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> tab
Then I see the <b>Activate</b> action next to a blocked user

When I click <b>Activate</b>
Then I see a confirmation dialog

When I click Continue
Then I see the dialog is closed
  And I see a notification message that the user has been OR has not been activated
  And I see the user’s status is changed to Active if the action was successful
  And I see the activated user can not view the comments and comment
  And notification about activation is sent to the user’s email
</pre>

## Mockups

1. Admin user sees actions dropdown against blocked user

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions dropdown against blocked user:**

![Admin user sees actions dropdown against blocked user](/products/sport_news_portal/web_application_features/user_management/images/user_management_page_with_action_dropdown_for_blocked_user.png)

</details>

## Test cases

1. Verify that admin can activate blocked user on the Users page
2. Verify that admin can cancel activating blocked user on the Users page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can activate blocked user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a blocked user on the <b>Users</b> tab|1) On the right of an active user, click the <b>Activate</b> action</br>2) On the confirmation dialog, click <b>Continue</b></br>3) Log out as admin user</br>4) Log in as activated user</br>5) Go through pages with comments|1) The confirmation dialog appears</br>2) The user has the <b>Active</b> state. Notification about activation is sent to the user’s email</br>4) The user can log in</br>5) The user can see and write comments|

### **#2. Verify that admin can cancel activating blocked user on the Users page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a blocked user on the <b>Users</b> tab|1) On the right of an active user, click the <b>Activate</b> action</br>2) On the confirmation dialog, click <b>Cancel</b></br>3) Log out as admin user</br>4) Log in as activated user</br>5) Go through pages with comments|1) The confirmation dialog appears</br>2) The user stays in <b>Blocked</b> state</br>4) The user can log in</br>5) The user cannot write comments|
</details>
