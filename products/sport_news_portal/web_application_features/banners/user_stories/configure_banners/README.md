### Back to [Banners on the portal](../../) feature

# Allow admin users to configure banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure a list of banners
    So that users can see them while viewing the Sport News site

## Acceptance criteria

<pre>
Scenario: An admin user configures a list of banners
Given I am logged in as an admin user

When I view the <b>Banners</b> configuration page
Then I see the following:
  - Section with the <b>Banners</b> heading and the <b>+ New Banner</b> button under the header section
  - Search icon
  - <b>Open</b> and <b>Closed</b> tabs with the number of banners displayed next to the tab name, and the list of banners below
  - <b>Predefined Banners</b> section with a table which contains four predefined banners: <b>Facebook Video</b>, <b>Facebook Post</b>, <b>Lifestyle</b>, <b>Dealbook</b> with <b>Show/Hide</b> toggle for each of them

When I view the <b>Open</b> tab
Then I see a table with a list of the opened banners that contains:
  - Banner name
  - Banner status
  - Status filter
  - Category in which this banner should be displayed

When I click on <b>Status</b> drop-down for any banner
Then I see the action options:
  - <b>Publish</b> for non published banner
  - <b>Close</b> for published banner

When I click <b>Publish</b> for non published banner
Then I see the banner status is changed to <b>Published</b>

When I change the banner category
Then I see published in is updated with that category

When I click on any banner from the table
Then I see a banner preview block at the right side of the page with a banner photo

When I click on a published banner
Then I see a publish date of the banner in the preview section
  And the category drop-down is disabled

When I select an unpublished banner
Then I see the last update date of the banner and the <b>Edit</b> and <b>Delete</b> buttons in the preview section
  And the category drop-down is enabled

When I click <b>Edit</b>
Then I see the a picture section, banner name field, <b>Save</b> and <b>Delete</b> buttons

When I delete a picture or banner name and click <b>Save</b>
Then I see the error message that the banner name and picture must be present

When I click <b>+ New banner</b>
Then <b>+ New banner</b> dissapears
  And I see a picture section, banner name field, <b>Save</b> and <b>Cancel</b> buttons

When I fill in the banner name and click <b>Save</b>
Then I see a banner is displayed at the top of the banners table in <b>Not published</b> status and a fist category from the categories list is defaulted

When I view the <b>Closed</b> tab
Then I see a table with a list of closed banner names, close date, and category it was published in

When I select any banner from the table
Then I see a banner preview section on the right side of the page with a banner photo

When I hover over the banner in the table
Then I see the <b>Delete</b> button appears on the right of the banner row

When I click the <b>Delete</b> icon
Then the confirmation popover appears

When I click to delete on the confirmation popover
Then I see the banner is deleted
</pre>

## Mockups

1. Admin user sees Open tab on the Banners configuration page
2. Admin user sees Closed tab on the Banners configuration page
3. Admin user clicked + New banner and sees a banner form
4. Admin user clicked to edit banner and sees a pre-populated banner form
5. Admin user sees a category drop-down options
6. Admin user sees actions drop-down options for an unpublished banner
7. Admin user sees actions drop-down options for a published banner
8. Admin user sees a delete confirmation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Open tab on the Banners configuration page:**

![Admin user sees Open tab on the Banners configuration page](/products/sport_news_portal/web_application_features/banners/images/banners_open_tab.png)

**2. Admin user sees Closed tab on the Banners configuration page:**

![Admin user sees Closed tab on the Banners configuration page](/products/sport_news_portal/web_application_features/banners/images/banners_closed_tab.png)

**3. Admin user clicked + New banner and sees a banner form:**

![Admin user clicked + New banner and sees a banner form](/products/sport_news_portal/web_application_features/banners/images/new_banner_form.png)

**4. Admin user clicked + New banner and sees a banner form:**

![Admin user clicked + New banner and sees a banner form](/products/sport_news_portal/web_application_features/banners/images/edit_banner_form.png)

**5. Admin user sees a category drop-down options:**

![Admin user sees a category drop-down options](/products/sport_news_portal/web_application_features/banners/images/banner_category_options.png)

**6. Admin user sees actions drop-down options for an unpublished banner:**

![Admin user sees actions drop-down options for an unpublished banner](/products/sport_news_portal/web_application_features/banners/images/unpublished_banner_actions.png)

**7. Admin user sees actions drop-down options for a published banner:**

![Admin user sees actions drop-down options for a published banner](/products/sport_news_portal/web_application_features/banners/images/published_banner_actions.png)

**8. Admin user sees a delete confirmation popup:**

![Admin user sees a delete confirmation popup](/products/sport_news_portal/web_application_features/banners/images/delete_confirmation.png)

</details>

## Test cases

1. Verify the content of the Banners page
2. Verify the content of the Open tab on the Banners page
3. Verify the content of the Closed tab on the Banners page
4. Verify that it is not possible to save banner without Name
5. Verify that it is possible to save the banner with all valid data
6. Verify that it is possible to cancel the banner creation at any stage
7. Verify that it is possible to filter banners by Published status
8. Verify that it is possible to filter banners by Not Published state
9. Verify that it is not possible to edit or delete the Published banner
10. Verify that it is not possible to edit a category of the Published banner
11. Verify that it is possible to edit a category of the Not published banner
12. Verify that it is possible to edit the Not Published banner
13. Verify that it is possible to delete the Not published banner
14. Verify that it is possible to delete the closed banner
15. Verify that admin can publish a not published banner
16. Verify that admin can close a published banner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Banners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Examine the tabs on the page|1) There are two tabs: <b>Open</b> and <b>Closed</b>. The <b>Open</b> tab is active by default. Also, there is a <b>Predefined Banners</b> section with default banners <b>Facebook Video, Facebook Post, Lifestyle, Dealbook</b> with <b>Show/Hide toggle</b> for each of them|

### **#2. Verify the content of the Open tab on the Banners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Observe the content of the <b>Open</b> tab|1) There is a table with 3 columns: <b>Banner name</b>, <b>Status (Published/Not published)</b>, <b>Publish in</b> (category)|

### **#3. Verify the content of the Closed tab on the Banners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Observe the content of the <b>Closed</b> tab|1) There is a table with 3 columns: <b>Banner name</b>, <b>Closed date</b>, <b>Publish in</b> (category). The <b>Delete</b> icon appears in each column when hovering over|

### **#4. Verify that it is not possible to save banner without Name**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>New Banner</b> button</br>2) Leave the <b>Name</b> field empty</br>3) Click <b>Save</b> button|3) An error message appears. The banner is not saved|

### **#5. Verify that it is possible to save the banner with all valid data**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>New Banner</b> button</br>2) Fill in the <b>Name</b> field</br>3) Upload the photo</br>4) Click <b>Save</b> button|4) The banner is saved and appears on the <b>Open</b> tab in the <b>Not published</b> status|

### **#6. Verify that it is possible to cancel the banner creation at any stage**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>New Banner</b> button</br>2) Enter a banner’s name</br>3) Upload a photo</br>4) Click <b>Cancel</b>|4) Banner is not saved and doesn’t appear in the <b>Open</b> tab|

### **#7. Verify that it is possible to filter banners by Published status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Click <b>Status</b> filter</br>2) Select <b>Published</b>|2) Only published banners are shown in the table|

### **#8. Verify that it is possible to filter banners by Not Published state**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Click <b>Status</b> filter</br>2) Select <b>Not Published</b>|2) Only non-published banners are shown in the table|

### **#9. Verify that it is not possible to edit or delete the Published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There are published banners|1) Click on a published banner|1) In the banner section on the right side and information about the banner appears. There is a <b>Name</b>, <b>Picture</b>, and <b>Creation Date</b>. No possibility to edit or delete|

### **#10. Verify that it is not possible to edit a category of the Published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is a published banner|1) Click on the published banner</br>2) Try to change the category|2) It is not possible to change the category for the banner|

### **#11. Verify that it is possible to edit a category of the Not published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Click on the unpublished banner</br>2) Change the category|2) The category is changed|

### **#12. Verify that it is possible to edit the Not Published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Click on the unpublished banner</br>2) Click <b>Edit</b></br>3) Edit name</br>4) Upload new picture</br>5) Click <b>Save</b> button|5) All changes are saved. The banner appears on the <b>Open</b> tab with the <b>Not published</b> status|

### **#13. Verify that it is possible to delete the Not published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Click on the unpublished banner</br>2) Click <b>Delete</b> button</br>3) On the confirmation message, click <b>Delete</b> button|3) The banner is removed from the <b>Open</b> tab|

### **#14. Verify that it is possible to delete the closed banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is a closed banner|1) Click the <b>Closed</b> tab</br>2) Click on a banner</br>3) Click <b>Delete</b> button</br>4) On the confirmation message, click <b>Delete</b> button|4) The banner is removed from the <b>Closed</b> tab|

### **#15. Verify that admin can publish a not published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is an unpublished banner|1) Click on a not published banner</br>2) Click the <b>Publish</b> action|2) Banner state is changed to <b>Published</b>. The banner is available for users in the right category|

### **#16. Verify that admin can close a published banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- There is a published banner|1) Click on a published banner</br>2) Click the <b>Close</b> action|2) The banner moved to the Closed tab. The banner is not available for users in the category|

</details>
