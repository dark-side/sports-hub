### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to edit Lifestyle and Dealbook's article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to edit an existing article in Lifestyle and Dealbook

## Acceptance criteria

<pre>
Scenario: An admin user edits the existing unpublished article
Given I am logged in as an admin user

When I click the Lifestyle/Dealbook link on the admin side
Then I see the list of blocks with articles

When I hover over an unpublished article
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." the menu icon for published article
Then I do not see the <b>Edit</b> menu item

When I click "..." the menu icon for unpublished article
Then I see the <b>Edit</b> menu item present

When I select <b>Edit</b> menu item
Then I see a prepopulated edit form with the article details

When I click the Preview link button
Then I see how this article is shown on the new tab

When I make any changes in the form
Then I see the <b>Save</b> button is enabled

When I click <b>Save</b> button
Then I see the page with a list of the articles
  And I see that my updated article appears at the top of the list in <b>unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I confirm cancelation
Then I see the page with a list of the articles
  And changes to the article are not saved
</pre>

## Mockups

1. Admin user sees Lifestyle index page
2. Admin user sees Dealbook index page
3. Admin user sees article actions on Dealbook and Lifestyle index page
4. Admin user sees Lifestyle new article page
5. Admin user sees Dealbook new article page
6. Admin user sees a confirmation popup on canceling the edit form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Lifestyle index page:**

![Admin user sees Lifestyle index page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/lifestyle_index_page.png)

**2. Admin user sees Dealbook index page:**

![Admin user sees Dealbook index page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/dealbook_index_page.png)

**3. Admin user sees article actions on Dealbook and Lifestyle index page:**

![Admin user sees article actions on Dealbook and Lifestyle index page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/article_actions_index_page.png)

**4. Admin user sees Lifestyle new article page:**

![Admin user sees Lifestyle new article page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/lifestyle_new_article_page.png)

**5. Admin user sees Dealbook new article page:**

![Admin user sees Dealbook new article page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/dealbook_new_article_page.png)

**6. Admin user sees a confirmation popup on canceling the edit form:**

![Admin user sees a confirmation popup on canceling the edit form](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/confirmation_to_cancel.png)

</details>

## Test cases

1. Verify that admin is able to change a picture to the edited article
2. Verify that admin is not able to save the picture of invalid format to the edited article
3. Verify that admin is not able to save empty required fields to the edited article
4. Verify that admin is able to preview the edited article
5. Verify that admin is able to save the edited article with all valid data updated
6. Verify that the comments section can be hidden for the edited article
7. Verify that the comments section can be shown for the edited article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to change a picture to the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Lifestyle/Dealbook</b> configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) In the Picture section, click <b>+Add picture</b></br>4) Choose the picture with the valid format (.jpg, .png, .jpeg, .tif)</br>5) Click <b>Save</b> button|5) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in unpublished state|

### **#2. Verify that admin is not able to save the picture of invalid format to the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Lifestyle/Dealbook</b> configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) In the Picture section, click <b>+Add picture</b></br>4) Choose the picture with the invalid format (any file except .jpg, .png, .jpeg, .tif)</br>5) Click <b>Save</b> button|5) Changes to the Article are not saved. The validation message "Only .jpg, .png, .jpeg, .tif formats are allowed" is shown|

### **#3. Verify that admin is not able to save empty required fields to the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Delete data from the <b>Alt</b> field</br>4) Click <b>Save</b></br>5)Fill in <b>Alt</b> required field</br>6) In the <b>Article headline</b> required field, delete data</br>7) Click <b>Save</b> button</br>8) Fill in <b>Article headline</b> required field</br>9) In the <b>Caption</b> required field, delete data</br>10) Click <b>Save</b> button</br>11) Fill in <b>Caption</b> required field</br>12) In the <b>Content</b> required field, delete data</br>13) Click <b>Save</b> button|4) The required fields are highlighted in red</br>7) The required fields are highlighted in red</br>10) The required fields are highlighted in red</br>13) The required fields are highlighted in red</br>|

### **#4. Verify that admin is able to preview the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Make some changes</br>4) Click the <b>Preview</b> link</br>5) Click <b>Back to edit<b> page link|4) The article is shown as it will look for users</br>5) The article is back to edit mode|

### **#5. Verify that admin is able to save the edited article with all valid data updated**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Update all required fields</br>4) Click <b>Save</b> button|4) Admin user is redirected to the list of articles. Article is saved with all information and appears at the top of the list in unpublished state|

### **#6. Verify that the comments section can be hidden for the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is an unpublished article</br>- The <b>Comments</b> section is shown for article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Click the <b>Comments: Show</b> toggle</br>4)Click <b>Save</b> button|3) <b>Comments: Show</b> changed to <b>Hide</b></br>4) The article is saved with the hidden comments section|

### **#7. Verify that the comments section can be shown for the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is an unpublished article</br>- The <b>Comments</b> section is hidden for article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Click the <b>Comments: Hide</b> toggle</br>4)Click <b>Save</b> button|3) <b>Comments: Hide</b> changed to <b>Show</b></br>4) The article is saved with the shown comments section|
</details>