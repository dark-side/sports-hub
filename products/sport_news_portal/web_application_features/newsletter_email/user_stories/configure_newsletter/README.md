### Back to [Newsletter subscription](../../) feature

# Allow admin users to configure Newsletter footer sections

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to configure Newsletter footer sections

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures Newsletter footer sections</i></b>

Given I am logged in as an admin user

When I am on the <b>Footer</b> configuration page
Then I see <b>Newsletter</b> tab next to <b>Company info</b> and <b>Contributors</b>

When I view the <b>Newsletter</b> tab
Then I see the configuration table with a single row: <b>Sign up to receive the latest in sport news</b> which can not be deleted

When I enable the <b>Show/Hide</b> toggle in the configuration table
Then I see the <b>Newsletter</b> subscription input is visible for the site users

When I disable the <b>Show/Hide</b> toggle in the configuration table
Then I see the <b>Newsletter</b> subscription input is not visible for the site users

When I disable the <b>Show section</b> toggle
Then I see the <b>Newsletter</b> section is not visible for the site users

When I enable the <b>Show section</b> toggle
Then I see the <b>Newsletter</b> section is visible for the site users
</pre>

## Mockups

1. Admin user sees a Newsletter tab on the footer configuration page

<details>
  <summary>Click here to see mockups details</summary>

**1.  Admin user sees a Newsletter tab on the footer configuration page:**

![ Admin user sees a Newsletter tab on the footer configuration page](/products/sport_news_portal/web_application_features/newsletter_email/images/newsletter_configuration.png)

</details>

## Test cases

1. Verify that the Footer configuration page shows three tabs and admin can go to any of them
2. Verify that admin can hide links for the site users on the Newsletter tab by clicking Show for items
3. Verify that admin can show links for the site users in the Newsletter tab by clicking Hide for items
4. Verify that Sign up to receive the latest in sport news link cannot be deleted in the Newsletter tab
5. Verify that admin can hide the Newsletter column by disabling the Show section on the Newsletter tab
6. Verify that admin can unhide the Newsletter column by enabling the Show section on the Newsletter tab
7. Verify that admin cannot edit content for the Sign up to receive the latest in sport news item in the Newsletter tab by clicking on it
8. Verify that admin cannot add a new item in the Newsletter tab. + New footer item button is not shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Footer configuration page shows three tabs and admin can go to any of them**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page|1) On the <b>Footer</b> configuration page, examine all tabs|1) There are three tabs shown: <b>Company info</b>, <b>Contributors</b>, <b>Newsletter</b>|

### **#2. Verify that admin can hide links for the site users on the Newsletter tab by clicking Show for items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab</br>- There are links which are shown for the users|1) Hover over the table row which is shown (footer link)</br>2) Turn on the <b>Show</b> toggle for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the hided footer link is not visible for the site user|1) Table row (footer link) becomes highlighted</br>2) The <b>Show</b> toggle is changed to <b>Hide</b></br>5) The appropriate item is not visible for the site user|

### **#3. Verify that admin can show links for the site users in the Newsletter tab by clicking Hide for items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab</br>- There are links which are hidden for the users|1) Hover over the table row which is hidden (footer link)</br>2) Turn on the <b>Hide</b> toggle for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the hided footer link is visible for the site user|1) Table row (footer link) becomes highlighted</br>2) The <b>Hide</b> toggle is changed to <b>Show</b></br>5) The appropriate item is visible for the site user|

### **#4. Verify that Sign up to receive the latest in sport news link cannot be deleted in the Newsletter tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab|1) Hover over the <b>Sign up to receive the latest in sport news</b> item|1) The <b>Delete</b> icon doesn’t appear|

### **#5. Verify that admin can hide the Newsletter column by disabling the Show section on the Newsletter tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab</br>- Show section toggle is enabled on the <b>Newsletter</b> tab|1) Turn off the <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Newsletter</b> column is present|4) The <b>Newsletter</b> column is not visible for the users|

### **#6. Verify that admin can unhide the Newsletter column by enabling the Show section on the Newsletter tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab</br>- Show section toggle is disabled on the <b>Newsletter</b> tab|1) Enable the <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Newsletter</b> column is present|4) The <b>Newsletter</b> column is visible for the users with all items which should be shown|

### **#7. Verify that admin cannot edit content for the Sign up to receive the latest in sport news item in the Newsletter tab by clicking on it**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab|1) Click on <b>Sign up to receive the latest in sport news</b> item in the table|1) The edit section is not opened on the right to the table|

### **#8. Verify that admin cannot add a new item in the Newsletter tab. + New footer item button is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Newsletter</b> tab|1) Examine the top right corner|1) Examine the top right corner|1) There is no <b>+ New footer item </b> button|

</details>
