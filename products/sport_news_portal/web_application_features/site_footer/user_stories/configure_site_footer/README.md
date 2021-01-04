### Back to [Site footer of the portal](../../) feature

# Allow admin users to configure site footer

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to configure site footer sections, links, and content

## Acceptance criteria

<pre>
Scenario: An admin user configures the links and columns of the site footer and the content of these links and columns
Given I am logged in as an admin user

When I am on the <b>Footer</b> configuration page
Then I see two tabs:
  - Company info
  - Contributors
  And I see the <b>Company info</b> tab is active by default
  And I see the active tab name is highlighted

When I view any of the tabs
Then I see the configuration table with the following columns:
  - Footer menu names
  - Hide/Show
  - Actions

When I view the <b>Company info</b> tab
Then I see the table contains the following rows (footer links):
  - About Sport News
  - News / In the Press
  - Advertising / Sports Blogger Ad Network
  - Events
  - Contact Us

When I hover over the <b>About Sport News</b> or <b>Contact Us</b> rows
The <b>Delete</b> icon does NOT appear

When I hover over the other table rows
Then I see the <b>Delete</b> icon

When I click <b>Delete</b>
Then I see the appropriate item is deleted and not visible

When I disable the <b>Show section</b> toggle
Then I see the whole <b>Company info</b> tab is not visible for the site users

When I enable the <b>Show section</b> toggle
Then I see the <b>Company info</b> tab is visible for the site users

When I click any item in the table
Then I see the edit section is opened on the right to the table
  And I see <b>Headline</b> text field, <b>Content</b> text area and <b>Cancel</b> and <b>Save</b> button

When I click <b>Contact Us</b> in the table
Then I see different edit form is opened on the right to the table
  And I see three fields: <b>Address</b>, <b>Telephone</b>, <b>Email</b>

When I edit some information there and click <b>Save</b>
Then the updated information is saved

When I click <b>+ New footer item</b> button
Then the popup to enter the link <b>Name</b> appears

When I enter the <b>Name</b> and click <b>Add</b>
Then the item is added to the <b>Company info</b> tab and open edit form is on the right side

When I view the <b>Company info</b> tab
Then I see the <b>Privacy and Terms</b> table below with thwo rows:
  - Privacy Policy
  - Terms and Conditions

When I click <b>Privacy policy</b> or <b>Terms and conditions</b> row
Then I see the edit section is opened on the right to the table
  And I see <b>Headline</b> text field, <b>Content</b> text area and <b>Cancel</b> and <b>Save</b> button

When I hover over the <b>Privacy policy</b> or <b>Terms and conditions</b> rows
The <b>Delete</b> button does NOT appear

When I view the <b>Contributors</b> tab
Then I see the configuration table with the following rows:
  - Featured Writers Program
  - Featured Team Writers Program
  - Internship Program
  And I can configure this tab the same way as the <b>Company info</b> tab
</pre>

  <i>The <b>Newsletter</b> is described [in separate feature](/products/sport_news_portal/web_application_features/newsletter_email)</i>

## Mockups

1. Admin user clicked New footer item and sees a popup
2. Admin user sees an edit form for the menu item
3. Admin user sees an edit form for Contact us
4. Admin user sees Contributors tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user clicked New footer item and sees a popup:**

![Admin user clicked New footer item and sees a popup](/products/sport_news_portal/web_application_features/site_footer/images/new_footer_item_popup.png)

**2. Admin user sees an edit form for the menu item:**

![Admin user sees an edit form for the menu item](/products/sport_news_portal/web_application_features/site_footer/images/new_footer_item_form.png)

**3. Admin user sees an edit form for Contact us:**

![Admin user sees an edit form for Contact us](/products/sport_news_portal/web_application_features/site_footer/images/footer_contact_us_form.png)

**4. Admin user sees Contributors tab:**

![Admin user sees Contributors tab](/products/sport_news_portal/web_application_features/site_footer/images/footer_contributors_tab.png)

</details>

## Test cases

1. Verify that the Footer configuration page shows two tabs and admin can go to any of them
2. Verify that admin can hide links for the site users in the Company info tab by clicking Show for items
3. Verify that admin can show links for the site users in the Company info tab by clicking Hide for items
4. Verify that links can be deleted in the Company info tab by clicking the Delete button
5. Verify that links About Sport News and Contact Us cannot be deleted in the Company info tab
6. Verify that admin can hide the Company info column by disabling the Show section on the Company info tab
7. Verify that admin can unhide the Company Info column by enabling the Show section in the Company info tab
8. Verify that admin can edit content for the items in the Company info tab by clicking on items
9. Verify that admin can add a new item in the Company info tab by clicking + New footer item button
10. Verify that admin can hide links for the site users in the Contributors tab by clicking Show for items
11. Verify that admin can show links for the site users in the Contributors tab by clicking Hide for items
12. Verify that links can be deleted in the Contributors tab by clicking the Delete button
13. Verify that admin can hide the Contributors column by disabling the Show section in the Contributors tab
14. Verify that admin can unhide the Contributors column by enabling the Show section on the Contributors tab
15. Verify that admin can edit content for the items in the Contributors tab by clicking on items
16. Verify that admin can add a new item in the Contributors tab by clicking + New footer item button
17. Verify that links Privacy Policy and Terms and Conditions cannot be deleted in the Privacy and Terms table
18. Verify that links Privacy Policy and Terms and Conditions cannot be hidden in the Privacy and Terms tab
19. Verify that admin can edit content for the items in the Privacy and Terms tab by clicking on items

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Footer configuration page shows two tabs and admin can go to any of them**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page|1) On the <b>Footer</b> configuration page, examine all tabs</br>2) Select the <b>Contributors</b> tab|1) There are two tabs shown: <b>Company info</b>, <b>Contributors</b>. <b>Company info</b> is opened by default and highlighted.  The Privacy and Terms table is on <b>Company info</b> page</br>2) The <b>Contributors</b> tab is opened and highlighted|

### **#2. Verify that admin can hide links for the site users in the Company info tab by clicking Show for items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab</br>- There are links which are shown for the users|1) Hover over the table row which is shown (footer link)</br>2) Click <b>Show</b> toggle for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the hided footer link is not visible for a site user|1) Table row (footer link) becomes highlighted</br>2) The <b>Show</b> toggle is switched to <b>Hide</b></br>5) The appropriate item is not visible for the site user|

### **#3. Verify that admin can show links for the site users in the Company info tab by clicking Hide for items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab</br>- There are links that are hidden for the users|1) Hover over the table row which is hidden (footer link)</br>2) Click <b>Hide</b> toggle for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the shown footer link is visible for a site user|1) Table row (footer link) becomes highlighted</br>2) The <b>Hide</b> toggle is switched to <b>Show</b></br>5) The appropriate item is visible for the site user|

### **#4. Verify that links can be deleted in the Company info tab by clicking the Delete button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab</br>- There are links which are shown for the users|1) Hover over the table row which is shown (footer link)</br>2) Click on <b>Delete</b> icon for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the deleted footer link is not visible for the site user|1) Table row (footer link) becomes highlighted</br>2) The appropriate item is deleted and no longer available for admin configuration</br>5) The appropriate item is not visible for the site user|

### **#5. Verify that links About Sport News and Contact Us cannot be deleted in the Company info tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab</br>- There are links which are shown for the users|1) Hover over the <b>About Sport News</b> (footer link)</br>2) Hover over the <b>Contact Us</b> (footer link)|1) The <b>Delete</b> icon doesn’t appear</br>2) The <b>Delete</b> icon doesn’t appear|

### **#6. Verify that admin can hide the Company info column by disabling the Show section on the Company info tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab</br>- <b>Show section</b> toggle is enabled on the <b>Company info</b> tab|1) Disable the <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Company info</b> column is present|4) The <b>Company info</b> column is not visible for the users|

### **#7. Verify that admin can unhide the Company Info column by enabling the Show section in the Company info tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab</br>- <b>Show section</b> toggle is disabled on the <b>Company info</b> tab|1) Enable the <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Company info</b> column is present|4) The <b>Company info</b> column is visible for the users with all items which should be shown|

### **#8. Verify that admin can edit content for the items in the Company info tab by clicking on items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab|1) Click any item in the table</br>2) Edit information</br>3) Click save button|1) The edit section is opened on the right to the table</br>3) The appropriate item is saved and edited information is visible for the site user|

### **#9. Verify that admin can add a new item in the Company info tab by clicking + New footer item button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Company info</b> tab|1) Click <b>New footer item</b> button</br>2) Enter name</br>3) Click <b>Add</b> button|1) The <b>Add new footer item</b> popup appears with a field to enter <b>Name</b> and <b>Cancel</b> and <b>Add</b> buttons</br>3) The appropriate item is added into the <b>Company info</b> tab and can be edited|

### **#10. Verify that admin can hide links for the site users in the Contributors tab by clicking Show for items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab</br>- There are links which are shown for the users|1) Hover over the table row which is shown (footer link)</br>2) Turn off the <b>Show</b> toggle for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the hided footer link is not visible for a site user|1) Table row (footer link) becomes highlighted</br>2) The <b>Show</b> toggle is switched to <b>Hide</b></br>5) The appropriate item is not visible for the site user|

### **#11. Verify that admin can show links for the site users in the Contributors tab by clicking Hide for items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab</br>- There are links which are hidden for the users|1) Hover over the table row which is hidden (footer link)</br>2) Turn on the <b>Hide</b> toggle for the hovered table row (footer link)</br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the shown footer link is visible for a site user|1) Table row (footer link) becomes highlighted</br>2) The <b>Hide</b> toggle is switched to <b>Show</b></br>5) The appropriate item is visible for the site user|

### **#12. Verify that links can be deleted in the Contributors tab by clicking the Delete button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab</br>- There are links which are shown for the users|1) Hover over the table row which is shown (footer link)</br>2) In the hovered table row (footer link), click <b>Delete</b></br>3) Log out by admin account</br>4) Log in by user account</br>5) Examine if the deleted footer link is not visible for a site user|1) Table row (footer link) becomes highlighted</br>2) The appropriate item is deleted and no longer available for admin configuration</br>5) The appropriate item is not visible for the site user|

### **#13. Verify that admin can hide the Contributors column by disabling the Show section in the Contributors tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab</br>- <b>Show section</b> toggle is enabled on the <b>Contributors</b> tab|1) Disable the <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Contributors</b> column is present|4) The <b>Contributors</b> column is not visible for the users|

### **#14. Verify that admin can unhide the Contributors column by enabling the Show section on the Contributors tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab</br>- <b>Show section</b> toggle is disabled on the <b>Contributors</b> tab|1) Enable the <b>Show section</b> toggle</br>2) Log out by admin account</br>3) Log in by user account</br>4) Examine if the <b>Contributors</b> column is present|4) The <b>Contributors</b> column is visible for the users with all items which should be shown|

### **#15. Verify that admin can edit content for the items in the Contributors tab by clicking on items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab|1) Click any item in the table</br>2) Edit information</br>3) Click save button|1) The edit section is opened on the right to the table</br>3) The appropriate item is saved and edited information is visible for the site user|

### **#16. Verify that admin can add a new item in the Contributors tab by clicking + New footer item button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Contributors</b> tab|1) Click <b>New footer item</b> button</br>2) Enter name</br>3) Click <b>Add</b> button|1) The <b>Add new footer item</b> popup appears with a field to enter <b>Name</b> and <b>Cancel</b> and <b>Add</b> buttons</br>3) The appropriate item is added into the <b>Contributors</b> tab and can be edited|

### **#17. Verify that links Privacy Policy and Terms and Conditions cannot be deleted in the Privacy and Terms table**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Privacy and Terms</b> table</br>- There are links which are shown for the users|1) Hover over the <b>Privacy Policy</b> (footer link)</br>2) Hover over the <b>Terms and Conditions</b> (footer link)|1) The <b>Delete</b> icon doesn’t appear</br>2) The <b>Delete</b> icon doesn’t appear|

### **#18. Verify that links Privacy Policy and Terms and Conditions cannot be hidden in the Privacy and Terms tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Privacy and Terms</b> table</br>- There are links which are shown for the users|1) Examine the <b>Privacy Policy</b> item</br>2) Examine the <b>Terms and Conditions</b> item|1) There is no <b>Show/Hide</b> toggle</br>2) There is no <b>Show/Hide</b> toggle</br>|

### **#19. Verify that admin can edit content for the items in the Privacy and Terms tab by clicking on items**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Footer</b> configuration page -> <b>Privacy and Terms</b> table|1) Click any item in the table</br>2) Edit information</br>3) Click save button|1) The edit section is opened on the right to the table</br>3) The appropriate item is saved and edited information is visible for the site user|

</details>
