### Back to [Manage articles on the portal](../../) feature

# Allow admin users to edit an existing article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to edit an existing article

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits the existing unpublished article</i></b>

Given I am logged in as an admin user

When I select any sports category link on the admin side
Then I see the list of blocks with articles

When I hover over an unpublished article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an unpublished article
Then I see the <b>Edit</b> menu item present

When I select the <b>Edit</b> menu item
Then I see the following:
  - Path to the article
  - Preview link button above the photo
  - Drag-and-drop field for image upload with <b>+ Add picture</b> link (required field)
  - Three drop-down fields, where I can select <b>Conference</b>, <b>Team</b>, and <b>Location</b>
  - Three required fields, where I can add details of the article: <b>Alt.</b>, <b>Article headline</b>, and <b>Caption</b>
  - HTML editor for content where I can format text (create a header, paragraph or list, manage font style and text aligning) (required field)
  - <b>Comments: Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> (disabled until I make any changes) buttons in the upper-right corner of the page

When I click the <b>Preview</b> link button
Then I see how this article is shown for users

When I hover over the <b>Picture</b> box
Then I see the icons for uploading a new image or editing the existing one (described in the story Editing the image of the article)

When I make any changes in the form
Then I see the <b>Save</b> button is enabled

When I click the <b>Save</b> button
Then I see the page with a list of the articles
  And I see that my updated article appears at the top of the list in <b>Unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I confirm cancelation
Then I see the page with a list of the articles
  And changes to the article are not saved

When I click the <b>Comments: Hide</b> toggle
Then the toggle changed to <b>Show</b>
And comments section is shown for users

When I click the <b>Comments: Show</b> toggle
Then the toggle changed to <b>Hide</b>
  And comments section is not shown for users
</pre>

## Mockups

1. Admin user sees an edit article form
2. Admin user sees a cancelation pop-up window
3. Admin user clicks the preview icon and sees a preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees an edit article form:**

![Admin user sees an edit article form](/products/sport_news_portal/web_application_features/manage_articles/images/article_filled_form.png)

**2. Admin user sees a cancelation pop-up window:**

![Admin user sees a cancelation pop-up window](/products/sport_news_portal/web_application_features/manage_articles/images/cancel_popup.png)

**3. Admin user clicks the preview icon and sees a preview page:**

![Admin user clicks the preview icon and sees a preview page](/products/sport_news_portal/web_application_features/manage_articles/images/article_preview_page.png)

</details>

## Test cases

1. Verify that admin is able to change a picture to the edited article
2. Verify that admin is not able to save the picture of invalid format to the edited article
3. Verify that admin is not able to save empty required fields to the edited article
4. Verify that admin is able to preview the edited article
5. Verify that admin is able to save the edited article with all valid data updated
6. Verify that admin is able to save changed the conference, team, and location for the edited article
7. Verify that the comments section can be hidden for the edited article
8. Verify that the comments section can be shown for the edited article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to change a picture to the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) In the <b>Picture</b> section, click <b>+Add picture</b></br>4) Choose the picture with the valid format (.jpg, .png, .jpeg, .tif)</br>5) Click <b>Save</b> button|5) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to save the picture of invalid format to the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) In the <b>Picture</b> section, click <b>+Add picture</b></br>4) Choose the picture with the invalid format (any file except .jpg, .png, .jpeg, .tif)</br>5) Click <b>Save</b>|5) Changes to the article are not saved. The validation message "Only .jpg, .png, .jpeg, .tif formats are allowed" appears|

### **#3. Verify that admin is not able to save empty required fields to the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) In the <b>Alt.</b> required field, delete data</br>4) Click <b>Save</b></br>5) Fill in <b>Alt.</b> required field</br>6) In the <b>Article headline</b> required field, delete data</br>7) Click <b>Save</b></br>8) Fill in <b>Article headline</b> required field</br>9) In the <b>Caption</b> required field, delete data</br>10) Click <b>Save</b></br>11) Fill in <b>Caption</b> required field</br>12) In the <b>Content</b> required field, delete data</br>13) Click <b>Save</b>|4) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>7) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>10) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>13) The required fields are highlighted in red. The validation message "Fill in all required fields" appears|

### **#4. Verify that admin is able to preview the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Make some changes</br>4) Change the conference, team, and location</br>5) Select the <b>Preview</b> link</br>6) Select <b>Back to edit page</b> link|5) The article is shown as it will look for users</br>6) The article is back to edit mode|

### **#5. Verify that admin is able to save the edited article with all valid data updated**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Update all required fields</br>4) Click <b>Save</b>|4) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in unpublished state|

### **#6. Verify that admin is able to save changed the conference, team, and location for the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Change a conference, team, and location</br>4) Click <b>Save</b>|4) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in unpublished state|

### **#7. Verify that the comments section can be hidden for the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article</br>- Comments section is shown for article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Click the <b>Comments: Show</b> toggle</br>4) Click <b>Save</b>|3) <b>Comments: Show</b> changed to <b>Hide</b></br>4) The article is saved with the hidden comments section|

### **#8. Verify that the comments section can be shown for the edited article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article</br>- Comments section is hidden for article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Click the <b>Comments: Hide</b> toggle</br>4) Click <b>Save</b>|3) <b>Comments: Hide</b> changed to <b>Show</b></br>4) The article is saved with the shown comments section|

</details>
