### Back to [Banners on the portal](../../README.md) feature

# Allow admin users to configure banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure a list of banners
    So that users can see them while viewing the Sports Hub site

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures a list of banners</i></b>

Given I am logged in as an admin user

When I view the <b>Banners</b> configuration page
Then I see the following:
  - Section with the <b>Banners</b> heading and the <b>+ New Banner</b> button under the header section
  - Search icon
  - <b>Opened</b> and <b>Closed</b> tabs with the number of banners displayed next to the tab name, and the list of banners below
  - <b>Predefined Banners</b> section with a table which contains four predefined banners: <b>Facebook Video</b>, <b>Facebook Post</b>, <b>Lifestyle</b>, <b>Dealbook</b> with the <b>Show/Hide</b> toggle for each of them

When I view the <b>Opened</b> tab
Then I see a table with a list of the opened banners that contains:
  - Banner name
  - Banner status
  - Status filter
  - Category in which this banner should be displayed

When I click <b>Status</b> drop-down list for any banner
Then I see the action options:
  - <b>Publish</b> for non published banner
  - <b>Close</b> for published banner

When I click <b>Publish</b> for non published banner
Then I see the banner status is changed to <b>Published</b>

When I change the banner category
Then I see published in is updated with that category

When I select any banner from the table
Then I see a banner preview block at the right side of the page with a banner photo

When I select a published banner
Then I see a publish date of the banner in the preview section
  And the category drop-down list is disabled

When I select an unpublished banner
Then I see the last update date of the banner and the <b>Edit</b> and <b>Delete</b> buttons in the preview section
  And the category drop-down list is enabled

When I click <b>Edit</b>
Then I see the a picture section, banner name field, <b>Save</b> and <b>Delete</b> buttons

When I delete a picture or banner name and click <b>Save</b>
Then I see the error message that the banner name and picture must be present

When I click <b>+ New banner</b>
Then <b>+ New banner</b> disappears
  And I see a picture section, banner name field, <b>Save</b> and <b>Cancel</b> buttons

When I enter the banner name and click <b>Save</b>
Then I see a banner is displayed at the top of the banners table in <b>Not published</b> status and a fist category from the categories list is defaulted

When I view the <b>Closed</b> tab
Then I see a table with a list of closed banner names, close date, and category it was published in

When I select any banner from the table
Then I see a banner preview section on the right side of the page with a banner photo

When I hover over the banner in the table
Then I see the <b>Delete</b> button appears on the right of the banner row

When I click <b>Delete</b>
Then the confirmation popover appears

When I confirm deleting on the popover
Then I see the banner is deleted
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Opened</b> tab on the <b>Banners</b> configuration page
2. Admin user sees the <b>Closed</b> tab on the <b>Banners</b> configuration page
3. Admin user clicked <b>+ New banner</b> and sees a banner form
4. Admin user clicked to edit banner and sees a pre-populated banner form
5. Admin user sees a category drop-down options
6. Admin user sees actions drop-down options for an unpublished banner
7. Admin user sees actions drop-down options for a published banner
8. Admin user sees a delete confirmation pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Opened tab on the Banners configuration page:**

![Admin user sees the Opened tab on the Banners configuration page](/desktop_application_features/banners/images/banners_open_tab.png)

**2. Admin user sees the Closed tab on the Banners configuration page:**

![Admin user sees the Closed tab on the Banners configuration page](/desktop_application_features/banners/images/banners_closed_tab.png)

**3. Admin user clicked + New banner and sees a banner form:**

![Admin user clicked + New banner and sees a banner form](/desktop_application_features/banners/images/new_banner_form.png)

**4. Admin user clicked to edit banner and sees a pre-populated banner form:**

![Admin user clicked to edit banner and sees a pre-populated banner form](/desktop_application_features/banners/images/edit_banner_form.png)

**5. Admin user sees a category drop-down options:**

![Admin user sees a category drop-down options](/desktop_application_features/banners/images/banner_category_options.png)

**6. Admin user sees actions drop-down options for an unpublished banner:**

![Admin user sees actions drop-down options for an unpublished banner](/desktop_application_features/banners/images/unpublished_banner_actions.png)

**7. Admin user sees actions drop-down options for a published banner:**

![Admin user sees actions drop-down options for a published banner](/desktop_application_features/banners/images/published_banner_actions.png)

**8. Admin user sees a delete confirmation pop-up window:**

![Admin user sees a delete confirmation pop-up window](/desktop_application_features/banners/images/delete_confirmation.png)

</details>

## Test cases

1. Verify the content of the <b>Banners</b> page
2. Verify the content of the <b>Opened</b> tab on the <b>Banners</b> page
3. Verify the content of the <b>Closed</b> tab on the <b>Banners</b> page
4. Verify that it is not possible to save the banner without name
5. Verify that it is possible to save the banner with all valid data
6. Verify that it is possible to cancel the banner creation at any stage
7. Verify that it is possible to filter banners by <b>Published</b> status
8. Verify that it is possible to filter banners by <b>Not published</b> status
9. Verify that it is not possible to edit or delete the published banner
10. Verify that it is not possible to edit a category of the published banner
11. Verify that it is possible to edit a category of the unpublished banner
12. Verify that it is possible to edit the unpublished banner
13. Verify that it is possible to delete the unpublished banner
14. Verify that it is possible to delete the closed banner
15. Verify that admin can publish the unpublished banner
16. Verify that admin can close the published banner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Banners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Examine the tabs on the page|1) There are two tabs: <b>Opened</b> and <b>Closed</b>. The <b>Opened</b> tab is active by default. Also, there is a <b>Predefined Banners</b> section with default banners <b>Facebook Video, Facebook Post, Lifestyle, Dealbook</b> with the <b>Show/Hide</b> toggle for each of them|

### **#2. Verify the content of the Opened tab on the Banners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Observe the content of the <b>Opened</b> tab|1) There is a table with 3 columns: <b>Banner name</b>, <b>Status (Published/Not published)</b>, <b>Published in</b> (category)|

### **#3. Verify the content of the Closed tab on the Banners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Observe the content of the <b>Closed</b> tab|1) There is a table with 3 columns: <b>Banner name</b>, <b>Closed date</b>, <b>Published in</b> (category). The <b>Delete</b> icon appears in each column when hovering over|

### **#4. Verify that it is not possible to save the banner without name**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>New Banner</b> button</br>2) Leave the <b>Name</b> field empty</br>3) Click <b>Save</b>|3) An error message appears. The banner is not saved|

### **#5. Verify that it is possible to save the banner with all valid data**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>New Banner</b> button</br>2) Fill in the <b>Name</b> field</br>3) Upload the photo</br>4) Click <b>Save</b>|4) The banner is saved and appears on the <b>Opened</b> tab in the <b>Not published</b> status|

### **#6. Verify that it is possible to cancel the banner creation at any stage**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>New Banner</b> button</br>2) Enter the banner name</br>3) Upload a photo</br>4) Click <b>Cancel</b>|4) The banner is not saved and doesn’t appear on the <b>Opened</b> tab|

### **#7. Verify that it is possible to filter banners by Published status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Click <b>Status</b> filter</br>2) Select <b>Published</b>|2) Only published banners are shown in the table|

### **#8. Verify that it is possible to filter banners by Not published status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Click <b>Status</b> filter</br>2) Select <b>Not published</b>|2) Only non-published banners are shown in the table|

### **#9. Verify that it is not possible to edit or delete the published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There are published banners|1) Select a published banner|1) The banner section on the right side and information about the banner appears. There is a <b>Name</b>, <b>Picture</b>, and <b>Creation date</b>. No possibility to edit or delete|

### **#10. Verify that it is not possible to edit a category of the published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is a published banner|1) Select the published banner</br>2) Try to change the category|2) It is not possible to change the category for the banner|

### **#11. Verify that it is possible to edit a category of the unpublished banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Select the unpublished banner</br>2) Change the category|2) The category is changed|

### **#12. Verify that it is possible to edit the unpublished banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Select the unpublished banner</br>2) Click <b>Edit</b></br>3) Edit name</br>4) Upload new picture</br>5) Click <b>Save</b>|5) All changes are saved. The banner appears on the <b>Opened</b> tab with the <b>Not published</b> status|

### **#13. Verify that it is possible to delete the unpublished banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Select the unpublished banner</br>2) Click <b>Delete</b></br>3) On the confirmation message, click <b>Delete</b>|3) The banner is removed from the <b>Opened</b> tab|

### **#14. Verify that it is possible to delete the closed banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is a closed banner|1) Click the <b>Closed</b> tab</br>2) Select a banner</br>3) Click <b>Delete</b></br>4) On the confirmation message, click <b>Delete</b>|4) The banner is removed from the <b>Closed</b> tab|

### **#15. Verify that admin can publish the unpublished banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Select the unpublished banner</br>2) Click the <b>Publish</b> action|2) Banner state is changed to <b>Published</b>. The banner is available for users in the right category|

### **#16. Verify that admin can close the published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is a published banner|1) Select a published banner</br>2) Click the <b>Close</b> action|2) The banner moved to the <b>Closed</b> tab. The banner is not available for users in the category|

</details>
