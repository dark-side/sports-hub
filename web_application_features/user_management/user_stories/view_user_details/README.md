### Back to [User management on the portal](../../README.md) feature

# Allow admin user to view user details on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view user details on the portal

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views user details</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I select user on the <b>Users</b> or <b>Admins</b> tab
Then I see a user details displayed on the right
  And I see two tabs with <b>General Info</b> and <b>Teams</b> details

When I click <b>General Info</b> tab
Then I see:
  - User's name
  - User's profile photo
  - Online/ofline status
  - <b>Registered</b> date
  - The amount of <b>Passed surveys</b>
  - The amount of the <b>Teams</b>

When I click <b>Teams</b> tab
Then I see a list of the teams that user follows

</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>General Info</b> tab
2. Admin user sees <b>Teams</b> tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees users being online/offline:**

![Admin user sees users being online/offline](/web_application_features/user_management/images/general_info_tab.png)

**2. Admin user sees Teams tab:**

![Admin user sees Teams tab](/web_application_features/user_management/images/teams_tab.png)

</details>

## Test cases

1. Verify that admin can see <b>General Info</b> of the selected user
2. Verify that admin can see <b>Teams</b> of the selected user

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can see General Info of the selected user**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a list of users|1) Select one of the users|1) The system displays a box on the right that shows <b>General Info</b> tab as active with the following details:</br>- User's name</br>- User's profile photo</br>- Online/ofline status</br>- <b>Registered</b> date</br>- The amount of <b>Passed surveys</b></br>- The amount of the <b>Teams</b>|

### **#2. Verify that admin can see Teams of the selected user**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is a list of users|1) Select one of the users</br>2) Select <b>Teams</b> tab|1) The system displays a box on the right that shows <b>General Info</b> tab as active</br>2) The system displays a list of the teams that user follows with a scrollbar|
</details>
