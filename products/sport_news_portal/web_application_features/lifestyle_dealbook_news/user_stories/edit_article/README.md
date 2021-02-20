### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to edit Lifestyle and Dealbook's articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to edit existing articles in Lifestyle and Dealbook

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits the existing unpublished article</i></b>

Given I am logged in as an admin user

When I select the <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the list of blocks with articles

When I hover over an unpublished article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click <b>...</b> the menu icon for published article
Then I do not see the <b>Edit</b> menu item

When I click <b>...</b> the menu icon for unpublished article
Then I see the <b>Edit</b> menu item is present

When I select the <b>Edit</b> menu item
Then I see a prepopulated edit form with the article details

When I select the <b>Preview</b> link button
Then I see how this article is shown on the new tab

When I make any changes in the form
Then I see the <b>Save</b> button is enabled

When I click <b>Save</b>
Then I see the page with a list of the articles
  And I see that my updated article appears at the top of the list in <b>Unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I confirm cancelation
Then I see the page with a list of the articles
  And changes to the article are not saved
</pre>

## Mockups

1. Admin user sees <b>Lifestyle</b> index page
2. Admin user sees <b>Dealbook</b> index page
3. Admin user sees article actions on <b>Dealbook</b> and <b>Lifestyle</b> index pages
4. Admin user sees <b>Lifestyle</b> new article page
5. Admin user sees <b>Dealbook</b> new article page
6. Admin user sees a confirmation pop-up window on canceling the edit form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Lifestyle index page:**

![Admin user sees Lifestyle index page](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/lifestyle_index_page.png)

**2. Admin user sees Dealbook index page:**

![Admin user sees Dealbook index page](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/dealbook_index_page.png)

**3. Admin user sees article actions on Dealbook and Lifestyle index pages:**

![Admin user sees article actions on Dealbook and Lifestyle index pages](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/article_actions_index_page.png)

**4. Admin user sees Lifestyle new article page:**

![Admin user sees Lifestyle new article page](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/lifestyle_new_article_page.png)

**5. Admin user sees Dealbook new article page:**

![Admin user sees Dealbook new article page](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/dealbook_new_article_page.png)

**6. Admin user sees a confirmation pop-up window on canceling the edit form:**

![Admin user sees a confirmation pop-up window on canceling the edit form](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/confirmation_to_cancel.png)

</details>

## Test cases

1. Verify that admin is able to change the picture in the edited article
2. Verify that admin is not able to save the picture of invalid format in the edited article
3. Verify that admin is not able to save empty required fields in the edited article
4. Verify that admin is able to preview the edited article
5. Verify that admin is able to save the edited article with all valid data updated
6. Verify that the comments section can be hidden in the edited article
7. Verify that the comments section can be shown in the edited article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to change the picture in the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Lifestyle</b> and <b>Dealbook</b> configuration pages</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) In the <b>Picture</b> section, click <b>+Add picture</b></br>4) Choose the picture with the valid format (.jpg, .png, .jpeg, .tif)</br>5) Click <b>Save</b>|5) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to save the picture of invalid format in the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Lifestyle</b> and <b>Dealbook</b> configuration pages</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) In the <b>Picture</b> section, click <b>+Add picture</b></br>4) Choose the picture with the invalid format (any file except .jpg, .png, .jpeg, .tif)</br>5) Click <b>Save</b>|5) Changes to the article are not saved. The validation message "Only .jpg, .png, .jpeg, .tif formats are allowed" appears|

### **#3. Verify that admin is not able to save empty required fields in the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) Delete data from the <b>Alt.</b> field</br>4) Click <b>Save</b></br>5)Fill in the <b>Alt.</b> required field</br>6) In the <b>Article headline</b> required field, delete data</br>7) Click <b>Save</b></br>8) Fill in <b>Article headline</b> required field</br>9) In the <b>Caption</b> required field, delete data</br>10) Click <b>Save</b></br>11) Fill in the <b>Caption</b> required field</br>12) In the <b>Content</b> required field, delete data</br>13) Click <b>Save</b>|4) The required fields are highlighted in red</br>7) The required fields are highlighted in red</br>10) The required fields are highlighted in red</br>13) The required fields are highlighted in red</br>|

### **#4. Verify that admin is able to preview the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) Make some changes</br>4) Select the <b>Preview</b> link</br>5) Select <b>Back to edit page</b> link|4) The article is shown as it will look for users</br>5) The article is back to edit mode|

### **#5. Verify that admin is able to save the edited article with all valid data updated**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) Update all required fields</br>4) Click <b>Save</b>|4) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#6. Verify that the Comments section can be hidden in the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article</br>- The <b>Comments</b> section is shown for article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) Click the <b>Comments: Show</b> toggle</br>4)Click <b>Save</b>|3) <b>Comments: Show</b> changed to <b>Hide</b></br>4) The article is saved with the hidden <b>Comments</b> section|

### **#7. Verify that the Comments section can be shown in the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article</br>- The <b>Comments</b> section is hidden for article|1) Hover over an unpublished article</br>2) Click <b>...</b> button > <b>Edit</b> menu item</br>3) Click the <b>Comments: Hide</b> toggle</br>4)Click <b>Save</b>|3) <b>Comments: Hide</b> changed to <b>Show</b></br>4) The article is saved with the shown <b>Comments</b> section|
</details>
