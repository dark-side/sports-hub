### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to add new articles to Lifestyle and Dealbook

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to add new articles to Lifestyle and Dealbook

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user creates a new article in Lifestyle and Dealbook</i></b>

Given I am logged in as an admin user

When I select the <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the <b>+ New Article</b> button in the upper-right corner of the page

When I click the <b>+ New Article</b> button
Then the new article page appears

When I view the new article page
Then I see the next elements:
  - Preview icon in the upper-right corner of the page
  - Drag-and-drop field for image upload with <b>+ Add picture</b> link (edit picture behavior should be the same as described in <b>Manage Articles - Allow admin users to have advanced editing of the article image</b>)
  - Three fields where I can add details of the article: <b>Alt., Article headline</b>, and <b>Caption</b>
  - HTML editor for article content
  - The <b>Comments: Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> (disabled until all required fields are filled) buttons in the upper-right corner of the page
  And all fields are required

When I click the preview icon
Then I see how this article is shown for the users

When I click <b>+ Add picture</b> inside the form for image upload
Then I see the file explorer window where I can select the needed image

When I hover over the selected picture
Then I see the icons for uploading a new image or editing the existing one (described in the story <b>Manage Articles - Allow admin users to have advanced editing of the article image</b>)

When I complete the form with all required fields
Then I see the <b>Save</b> button is enabled

When I click <b>Save</b>
Then I see the page with a list of the articles
  And I see that my article is added at the top of the list in <b>Unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I confirm cancelation
Then I see the page with a list of the articles
  And the article is not saved

When I click the <b>Comments: Hide</b> toggle
Then the toggle changed to <b>Show</b>
  And the <b>Comments</b> section is shown for users

When I click the <b>Comments: Show</b> toggle
Then the toggle changed to <b>Hide</b>
  And the <b>Comments</b> section is not shown for users
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees a <b>Lifestyle</b> list of articles
2. Admin user sees a <b>Dealbook</b> list of articles
3. Admin user sees <b>Lifestyle</b> new article page
4. Admin user sees <b>Dealbook</b> new article page
5. Admin user sees a confirmation pop-up window on canceling the edit form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a Lifestyle list of articles:**

![Admin user sees a Lifestyle list of articles](/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/lifestyle_index_page.png)

**2. Admin user sees a Dealbook list of articles:**

![Admin user sees a Dealbook list of articles](/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/dealbook_index_page.png)

**3. Admin user sees Lifestyle new article page:**

![Admin user sees Lifestyle new article page](/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/lifestyle_new_article_page.png)

**4. Admin user sees Dealbook new article page:**

![Admin user sees Dealbook new article page](/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/dealbook_new_article_page.png)

**5. Admin user sees a confirmation pop-up window on canceling the edit form:**

![Admin user sees a confirmation pop-up window on canceling the edit form](/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/confirmation_to_cancel.png)

</details>

## Test cases

1. Verify that admin is able to add photos to new articles
2. Verify that admin is not able to upload photos of invalid format to new articles
3. Verify that admin is not able to save new articles when required fields are not filled
4. Verify that admin is not able to save new articles without uploading photos
5. Verify that admin is able to preview new articles
6. Verify that admin is able to save new articles with all required fields filled in
7. Verify that the <b>Comments</b> section can be hidden in new articles
8. Verify that the <b>Comments</b> section can be shown in new articles

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to add photos to new articles**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) In the Picture section, click <b>+Add picture</b></br>3) Choose a photo with the valid format (.jpg, .png, .jpeg, .tif)</br>4) Fill in all required boxes</br>5) Click <b>Save</b>|5) Admin user is redirected to the list of articles. The article is saved and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to upload photos of invalid format to new articles**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) In the Picture section, click <b>+Add picture</b></br>3) Choose a photo with the invalid format (any file except .jpg, .png, .jpeg, .tif)</br>4) Fill in all required boxes</br>5) Click <b>Save</b>|5) The validation message "Only .jpg, .png, .jpeg, .tif formats are allowed" appears|

### **#3. Verify that admin is not able to save new articles when required fields are not filled**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) In the <b>Picture</b> section, click <b>+Add picture</b></br>3) Select a photo with the valid format (.jpg, .png, .jpeg, .tif)</br>4) Do not fill in the <b>Alt.</b> required field</br>5) Fill in all the rest required fields</br>6) Click <b>Save</b></br>7) Do not fill in the <b>Article headline</b> required field</br>8) Fill in all the rest required fields</br>9) Click <b>Save</b></br>10) Do not fill in the <b>Caption</b> required field</br>11) Fill in all the rest required fields</br>12) Click <b>Save</b></br>13) Do not fill in the <b>Content</b> required field</br>14) Fill in all the rest required field</br>15) Click <b>Save</b>|6) The required fields are highlighted in red</br>9) The required fields are highlighted in red</br>12) The required fields are highlighted in red</br>15) The required fields are highlighted in red|

### **#4. Verify that admin is not able to save new articles without uploading photos**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) Do not upload file</br>3) Fill in all required fields</br>4) Click <b>Save</b>|4) The <b>Picture</b> field is highlighted in red|

### **#5. Verify that admin is able to preview new articles**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click <b>Preview</b></br>4) Click <b>Back to edit page</b>|3) The article is shown as it will look for users</br>4) The article is back to edit mode|

### **#6. Verify that admin is able to save new articles with all required fields filled in**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click <b>Save</b>|3) Admin user is redirected to the list of articles. The article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#7. Verify that the Comments section can be hidden in new articles**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click the <b>Comments: Show</b> toggle</br>4) Click <b>Save</b>|3) The <b>Comments</b> toggle changed to <b>Hide</b></br>4) The article is saved but the <b>Comments</b> section is not visible to users|

### **#8. Verify that the Comments section can be shown in new articles**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) The <b>Comments:</b> toggle is in <b>Show</b> state</br>4) Click <b>Save</b>|4) The article is saved with <b>Comments</b> section visible to users|

</details>
