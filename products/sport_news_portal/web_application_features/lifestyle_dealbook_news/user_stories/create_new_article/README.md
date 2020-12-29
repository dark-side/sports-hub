### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to add the new article to Lifestyle and Dealbook

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to add the new article to Lifestyle and Dealbook

## Acceptance criteria

<pre>

Scenario: An admin user creates a new article in Lifestyle/Dealbook
Given I am logged in as an admin user

When I click the <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the <b>+ New Article</b> button in the upper-right corner of the page

Then I see the following:
  - <b>+ New Article</b> button in the upper-right corner of the page
  - A filter by status and a search field
  - The list of blocks – one block per one existing article – where each block has:
    - Article thumbnail photo on the left side
    - Article headline on the right from the photo
    - First few sentences of the article
  - Status of the article (<b>Published</b> or not)
  - The scroll bar next to the list of articles

When I scroll the list of the articles
Then I see a list of articles is appended with a new portion of articles

When I hover over an article
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." button
Then I see the following options:
  - <b>Unpublish</b> if the article is published or <b>Publish</b> if the article is unpublished
  - <b>Edit</b>
  - <b>Delete</b>

When I click the <b>+ New Article</b> button
Then the new article page appears

When I view the new article page
Then I see the next elements:
  - Preview icon in the upper-right corner of the page
  - Drag-and-drop field for image upload with <b>+ Add picture</b> link (edit picture behavior should be the same as described in ![Manage Articles - Allow admin users to edit the image of the article](/products/sport_news_portal/web_application_features/manage_articles/user_stories/edit_article_image))
  - Three fields, where I can add details of the article: <b>Alt, Article headline</b>, and <b>Caption</b>
  - HTML editor for article content
  - <b>Comments: Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> (disabled until all required fields are filled) buttons in the upper-right corner of the page
  And all fields are required

When I click the preview icon
Then I see how this article is shown for the users

When I click <b>+ Add picture</b> inside the form for image upload
Then I see the file explorer window where I can select the needed image

When I hover over the selected picture
Then I see the icons for uploading a new image or editing the existing (described in the story Editing the image of the article)

When I complete the form with all required fields
Then I see the <b>Save</b> button is enabled

When I click <b>Save</b> button
Then I see the page with a list of the articles
  And I see that my article is added at the top of the list in <b>unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I confirm cancelation
Then I see the page with a list of the articles
  And article is not saved

When I click <b>Comments: Hide</b> toggle
Then the toggle changed to <b>Show</b>
  And <b>Comments</b> section is shown for users

When I click <b>Comments: Show</b> toggle
Then the toggle changed to <b>Hide</b>
  And <b>Comments</b> section is not shown for users
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

1. Verify the content of the Lifestyle/Dealbook index pages
2. Verify that list of articles is populated with new elements when it is scrolled down
3. Verify that admin is able to add photo to the new article
4. Verify that admin is not able to upload a photo of invalid format to the new article
5. Verify that admin is not able to save a new article when required boxes are not filled
6. Verify that admin is not able to save a new article without uploading a photo
7. Verify that admin is able to preview new article
8. Verify that admin is able to save the new article with all required fields filled in
9. Verify that the comments section can be hidden for a new article
10. Verify that the comments section can be shown for a new article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Lifestyle/Dealbook index pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Examine the index pages for Lifestyle and Dealbook|1) There are blocks of articles where each block has:</br>- Article thumbnail photo on the left side</br>- Article Headline on the right from the photo</br>- First few sentences of the article</br>- Status of the article (Published/Unpublished|

### **#2. Verify that list of articles is populated with new elements when it is scrolled down**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There are a lot of articles to load|1) Move through the list of articles</br>2) Check if the articles list is loaded|2) When an admin moves through the list of articles, the articles are loaded|

### **#3. Verify that admin is able to add photo to the new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b> button</br>2) In the Picture section, click <b>+Add picture</b></br>3) Choose the photo with the valid format (.jpg, .png, .jpeg, .tif)</br>4) Fill in all required boxes</br>5) Click <b>Save</b>|5) Admin user is redirected to the list of articles. Article is saved and appears at the top of the list in Unpublished state|

### **#4. Verify that admin is not able to upload a photo of invalid format to the new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b> button</br>2) In the Picture section, click <b>+Add picture</b></br>3) Choose the photo with the invalid format (any file except .jpg, .png, .jpeg, .tif)</br>4) Fill in all required boxes</br>5) Click <b>Save</b>|5) The validation message "Only .jpg, .png, .jpeg, .tif formats are allowed" is shown|

### **#5. Verify that admin is not able to save a new article when required boxes are not filled**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b></br>2) In the <b>Picture</b> section, click <b>+Add picture</b></br>3) Select a photo with the valid format (.jpg, .png, .jpeg, .tif)</br>4) Do not fill in the <b>Alt</b> required field</br>5) Fill in all the rest required fields</br>6) Click <b>Save</b></br>7) Do not fill in the Article headline required field</br>8) Fill in all the rest required fields</br>9) Click <b>Save</b></br>10) Do not fill in the Caption required field</br>11) Fill in all the rest required fields</br>12) Click <b>Save</b></br>13) Do not fill in the <b>Content</b> required field</br>14) Fill in all the rest required field</br>15) Click <b>Save</b>|6) The required fields are highlighted in red</br>9) The required fields are highlighted in red</br>12) The required fields are highlighted in red</br>15) The required fields are highlighted in red|

### **#6. Verify that admin is not able to save a new article without uploading a photo**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b></br>2) Do not upload file</br>3) Fill in all required fields</br>4) Click <b>Save</b>|4) The Picture field is highlighted in red|

### **#7. Verify that admin is able to preview new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click <b>Preview</b></br>4) Click <b>Back to edit</b> page button|3) The article is shown as it will look for users</br>4) The article is back to edit mode|

### **#8. Verify that admin is able to save the new article with all required fields filled in**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click <b>Save</b>|3) Admin user is redirected to the list of articles. Article is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#9. Verify that the comments section can be hidden for a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) Click <b>Comments: Show</b> toggle</br>4) Click <b>Save</b>|3) The <b>Comments</b> toggle changed to <b>Hide</b></br>4) The article is saved but the <b>Comments</b> section is not shown for users|

### **#10. Verify that the comments section can be shown for a new article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Click <b>+ New Article</b></br>2) Fill in all required fields</br>3) The <b>Comments:</b>  toggle is in <b>Show</b> state</br>4) Click <b>Save</b>|4) The article is saved with <b>Comments</b> section shown for users|

</details>
