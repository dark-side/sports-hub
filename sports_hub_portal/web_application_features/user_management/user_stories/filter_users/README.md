### Back to [User management on the portal](../../) feature

# Allow admin user to filter users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to filter users based on criteria
    So that I can perform the needed action

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user filters the users</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> tab
Then I see a filter with options: <b>Active, Blocked, Online, Offline</b>

When I select any option
Then I see a relevant result and the number of selected users
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the user management page with filter dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the user management page with filter dropdown:**

![Admin user sees the user management page with filter dropdown](/sports_hub_portal/web_application_features/user_management/images/user_management_page_with_filter_dropdown.png)

</details>

## Test cases

1. Verify that admin can filter users
2. Verify that admin can filter admins

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can filter users**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) Click the filter icon</br>2) Select <b>Active</b></br>3) Click the filter icon</br>4) Select <b>Blocked</b></br>5) Click the filter icon</br>6) Select <b>Online</b></br>7) Click the filter icon</br>8) Select <b>Offline</b>|2) Only active users are shown in the table</br>4) Only blocked users are shown in the table</br>6) Only online users are shown in the table</br>8) Only offline users are shown in the table|

### **#2. Verify that admin can filter admins**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) Select the <b>Admins</b> tab</br>2) Click the filter icon</br>3) Select <b>Online</b></br>4) Click the filter icon</br>5) Select <b>Offline</b>|3) Only online users are shown in the table</br>5) Only offline users are shown in the table|
</details>
