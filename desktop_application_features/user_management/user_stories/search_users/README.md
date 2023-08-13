### Back to [User management on the portal](../../README.md) feature

# Allow admin user to search users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to search users by name

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user filters the users</i></b>

Given I am logged in as an admin user

When I am on the <b>Users</b> configuration page
  And I view the <b>Users</b> tab
Then I see the search icon with the placeholder "Type a user name here"

When I enter the user’s name
Then I see the user that match the search
</pre>

<i>Search can start when the first symbol is entered or when at least 3 symbols are entered</i>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees search users input field when clicking the magnifier icon

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees search users input field when clicking the magnifier icon:**

![Admin user sees search users input field when clicking the magnifier icon](/desktop_application_features/user_management/images/user_management_page_with_search_input_field.png)

</details>

## Test cases

1. Verify that admin can search users

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can search users on the Users and Admins tabs**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page|1) In the search input, type some text</br>2) Click the <b>Admins</b> tab</br>3) In the search input, type some text|2) The list of users which match the entered text is shown</br>3) The list of admins that match the entered text is shown|
</details>
