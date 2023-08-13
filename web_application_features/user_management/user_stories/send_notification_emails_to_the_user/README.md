### Back to [User management on the portal](../../README.md) feature

# Send notification emails to users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to receive notification in my email
    So that I know if I was blocked, activated, got/lost admin permissions

## Acceptance criteria

<pre>
<b><i>Scenario: A site user receives notifications in email</i></b>

Given I am logged in as a site user

When I am blocked, activated, got/lost admin permissions by the admin user
Then I see an email with a corresponding message
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Example of the email style and structure

<details>
  <summary>Click here to see mockups details</summary>

**1. Example of the email style and structure:**

![Example of the email style and structure](/web_application_features/user_management/images/mail_style_example.png)

</details>

## Test cases

1. Verify that notification is sent to the user’s email in case of user changes

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that notification is sent to the user’s email in case of user changes**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Users</b> configuration page</br>- There is an active user on the <b>Users</b> tab</br>- There is a blocked user on the <b>Users</b> tab</br>- There is another admin on the <b>Admins</b> tab|1) Block the active user</br>2) Make the blocked user active</br>3) Set admin permissions for the active user</br>4) Remove admin permissions from another admin</br>5) Delete the active user</br>6) Delete the blocked user</br>7) Delete another admin|1)-4) The email about changes is sent to the users’ emails</br>5)-7) No emails about changes|
</details>
