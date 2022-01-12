### Back to [Newsletter subscription](../../) feature

# Allow admin user to configure Newsletter footer section

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to configure Newsletter footer section

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures Newsletter footer section</i></b>

Given I am logged in as an admin user

When I am on the <b>Footer</b> configuration page
Then I see <b>Newsletter</b> tab next to <b>Company info</b> and <b>Contributors</b>

When I view the <b>Newsletter</b> tab
Then I see the configuration table with a single row <b>Sign up to receive the latest sports news</b> which can not be deleted

When I enable the <b>Show/Hide</b> toggle in the configuration table
Then I see the <b>Newsletter</b> subscription input is visible to site users

When I disable the <b>Show/Hide</b> toggle in the configuration table
Then I see the <b>Newsletter</b> subscription input is not visible to site users

When I disable the <b>Show section</b> toggle
Then I see the <b>Newsletter</b> section is not visible to site users

When I enable the <b>Show section</b> toggle
Then I see the <b>Newsletter</b> section is visible to site users
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Newsletter</b> tab on the footer configuration page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Newsletter tab on the footer configuration page:**

![ Admin user sees the Newsletter tab on the footer configuration page](/sports_hub_portal/desktop_application_features/newsletter_email/images/newsletter_configuration.png)

</details>

## Test cases

1. Verify that the Footer configuration page shows three tabs and admin can go to any of them
2. Verify that admin can hide links from site users on the <b>Newsletter</b> tab by clicking <b>Show</b>
3. Verify that admin can show links to site users on the <b>Newsletter</b> tab by clicking <b>Hide</b>
4. Verify that the <b>Sign up to receive the latest sports news</b> link cannot be deleted on the <b>Newsletter</b> tab
5. Verify that admin can hide the <b>Newsletter</b> column by disabling the <b>Show section</b> on the <b>Newsletter</b> tab
6. Verify that admin can unhide the <b>Newsletter</b> column by enabling the <b>Show section</b> on the <b>Newsletter</b> tab
7. Verify that admin cannot edit content for the <b>Sign up to receive the latest sports news</b> link on the <b>Newsletter</b> tab by selecting it
8. Verify that admin cannot add a new page on the <b>Newsletter</b> tab. The <b>+ New footer page</b> button is not shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Footer configuration page shows three tabs and admin can go to any of them**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page|1) On the <b>Footer</b> configuration page, examine all tabs|1) There are three tabs shown: <b>Company info</b>, <b>Contributors</b>, <b>Newsletter</b>|

### **#2. Verify that admin can hide links from site users on the Newsletter tab by clicking Show**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab</br>- There are links which are visible to the users|1) Hover over the table row which is shown (footer link)</br>2) Turn on the <b>Show</b> toggle for the hovered table row (footer link)</br>3) Log out of admin account</br>4) Log in with user account</br>5) Examine if the hidden footer link is not visible to site users|1) Table row (footer link) becomes highlighted</br>2) The <b>Show</b> toggle is changed to <b>Hide</b></br>5) The appropriate item is not visible to site users|

### **#3. Verify that admin can show links to site users on the Newsletter tab by clicking Hide**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab</br>- There are links which are hidden for users|1) Hover over the table row which is hidden (footer link)</br>2) Turn on the <b>Hide</b> toggle for the hovered table row (footer link)</br>3) Log out of admin account</br>4) Log in with user account</br>5) Examine if the hidden footer link is visible to site users|1) Table row (footer link) becomes highlighted</br>2) The <b>Hide</b> toggle is changed to <b>Show</b></br>5) The appropriate item is visible to site users|

### **#4. Verify that the Sign up to receive the latest sports news link cannot be deleted on the Newsletter tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab|1) Hover over the <b>Sign up to receive the latest sports news</b> item|1) The <b>Delete</b> icon doesn’t appear|

### **#5. Verify that admin can hide the Newsletter column by disabling the Show section on the Newsletter tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab</br>- The <b>Show section</b> toggle is enabled on the <b>Newsletter</b> tab|1) Turn off the <b>Show section</b> toggle</br>2) Log out of admin account</br>3) Log in with user account</br>4) Examine if the <b>Newsletter</b> column is present|4) The <b>Newsletter</b> column is not visible to users|

### **#6. Verify that admin can unhide the Newsletter column by enabling the Show section on the Newsletter tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab</br>- The <b>Show section</b> toggle is disabled on the <b>Newsletter</b> tab|1) Enable the <b>Show section</b> toggle</br>2) Log out of admin account</br>3) Log in with user account</br>4) Examine if the <b>Newsletter</b> column is present|4) The <b>Newsletter</b> column is visible to users with all items which should be shown|

### **#7. Verify that admin cannot edit content for the Sign up to receive the latest sports news link on the Newsletter tab by selecting it**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab|1) Click <b>Sign up to receive the latest sports news</b> item in the table|1) The edit section is not opened on the right of the table|

### **#8. Verify that admin cannot add a new page on the Newsletter tab. The + New footer page button is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Footer</b> configuration page > <b>Newsletter</b> tab|1) Examine the top right corner|1) There is no <b>+ New footer page</b> button|

</details>
