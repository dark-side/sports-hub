### Back to [Manage articles on the portal](../../README.md) feature

# Allow admin users to add a new article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to add a new article

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user creates a new article</i></b>

Given I am logged in as an admin user

When I select any sports category link on the admin side
Then I see the <b>+ New Article</b> button in the upper-right corner of the page

When I click the <b>+ New Article</b> button
Then the new article page appears

When I view the new article page
Then I see the next elements:
  - The preview icon in the upper-right corner of the page
  - Drag-and-drop field for image upload with <b>+ Add picture</b> link (required field)
  - Three drop-down fields, where I can select <b>Subcategory</b>, <b>Team</b>, and <b>Location</b>
  - Three required fields, where I can add details of the article: <b>Alt.</b>, <b>Article headline</b>, and <b>Caption</b>
  - HTML editor for content where I can format text (create a header, paragraph or list, manage font style and text aligning) (required field)
  - <b>Comments: Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> (disabled until all fields are filled) buttons in the upper-right corner of the page

When I click the preview icon
Then I see how this article is shown for the users

When I click <b>+ Add picture</b> inside the form for image uploading
Then I see the file explorer window where I can select the needed image

When I complete the form with all required fields
Then I see the <b>Save</b> button is enabled

When I click the <b>Save</b> button
Then I see the page with the list of articles
  And I see that my article is added at the top of the list in <b>Unpublished</b> state

When I click the <b>Cancel</b> button
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I confirm cancelation
Then I see the page with a list of articles
  And the article is not saved

When I click <b>Comments: Hide</b> toggle
Then the toggle changed to <b>Show</b>
  And comments section is shown for users

When I click <b>Comments: Show</b> toggle
Then the toggle changed to <b>Hide</b>
  And comments section is not shown for users
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees a new article form
2. Admin user sees a filled in form
3. Admin user sees a cancelation pop-up window
4. Admin user clicks the preview icon and sees a preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a new article form:**

![Admin user sees a new article form](/web_application_features/manage_articles/images/article_empty_form.png)

**2. Admin user sees a filled in form:**

![Admin user sees a filled in form](/web_application_features/manage_articles/images/article_filled_form.png)

**3. Admin user sees a cancelation pop-up window:**

![Admin user sees a cancelation pop-up window](/web_application_features/manage_articles/images/cancel_popup.png)

**4. Admin user clicks the preview icon and sees a preview page:**

![Admin user clicks the preview icon and sees a preview page](/web_application_features/manage_articles/images/article_preview_page.png)

</details>

## Test cases

1. Verify that admin is able to add a picture to a new article
2. Verify that admin is not able to upload a picture of invalid format to a new article
3. Verify that admin is not able to save a new article when required boxes are not filled
4. Verify that admin is not able to save a new article without uploading a picture
5. Verify that admin is able to preview a new article
6. Verify that admin is able to save the new article with all required fields filled in
7. Verify that admin is able to select a subcategory, team, and location for a new article
8. Verify that the comments section can be hidden for a new article
9. Verify that the comments section can be shown for a new article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to add a picture to a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b> button</br>2) In the <b>Picture</b> section, click <b>+Add picture</b></br>3) Choose the picture with the valid format (.jpg, .png, .jpeg, .tif)</br>4) Fill in all required fields</br>5) Click <b>Save</b>|5) Admin user is redirected to the list of articles. The article is saved and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to upload a picture of invalid format to a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) In the <b>Picture</b> section, click <b>+Add picture</b></br>3) Choose the picture with the invalid format (any file format except .jpg, .png, .jpeg, .tif)</br>4) Fill in all required fields</br>5) Click <b>Save</b>|5) The validation message "Only .jpg, .png, .jpeg, .tif formats are allowed" appears|

### **#3. Verify that admin is not able to save a new article when required boxes are not filled**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) In the <b>Picture</b> section, click <b>+Add picture</b></br>3) Select a picture with the valid format (.jpg, .png, .jpeg, .tif)</br>4) Do not fill in the <b>Alt.</b> required field</br>5) Fill in all the rest required fields</br>6) Click <b>Save</b></br>7) Do not fill in the <b>Article headline</b> required field</br>8) Fill in all the rest required fields</br>9) Click <b>Save</b></br>10) Do not fill in the <b>Caption</b> required field</br>11) Fill in all the rest required fields</br>12) Click <b>Save</b></br>13) Do not fill in the <b>Content</b> required field</br>14) Fill in all the rest required fields</br>15) Click <b>Save</b>|6) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>9) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>12) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>15) The required fields are highlighted in red. The validation message "Fill in all required fields" appears|

### **#4. Verify that admin is not able to save a new article without uploading a picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) Do not upload file</br>3) Fill in all required fields</br>4) Click <b>Save</b>|4) The field is highlighted in red. The validation message "Please, upload a photo" is shown|

### **#5. Verify that admin is able to preview a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page |1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Change the subcategory, team, and location</br>4) Click the preview icon</br>5) Click the <b>Back to edit page</b> button|4) The article is shown as it will look for users</br>5) The article is back to edit mode|

### **#6. Verify that admin is able to save the new article with all required fields filled in**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click <b>Save</b>|3) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#7. Verify that admin is able to select a subcategory, team, and location for a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Change the subcategory, team, and location</br>4) Click <b>Save</b>|3) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#8. Verify that the comments section can be hidden for a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click the <b>Comments: Show</b> toggle</br>4) Click <b>Save</b>|3) The <b>Comments: Show</b> toggle changed to <b>Hide</b></br>4) The article is saved but the comments section is not shown for users|

### **#9. Verify that the comments section can be shown for a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click the <b>Comments: Hide</b> toggle</br>4) Click <b>Save</b>|4) The article is saved with the comments section shown for users|

</details>
