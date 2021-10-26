### Back to [Manage articles on the portal](../../) feature

# Allow admin users to have advanced editing of the article image

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have an advanced editor for the article image

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits an image of an article</i></b>

Given I am logged in as an admin user

When I hover over the <b>Picture</b> box on the <b>Add</b> or <b>Edit</b> article page
Then I see the picture editing icons:
  - Upload new image
  - Filters
  - Crop
  - Delete
  - Resize

When I click the filters icon
Then I see thumbnails with different filters
  And I see the name of each filter above the thumbnails
  And I see the <b>OK</b> and <b>Cancel</b> buttons

When I select the filter
Then I see the filter is applied to the picture

When I click <b>OK</b>
Then I see thumbnails disappear and I see the previous <b>Add</b> or <b>Edit</b> article page with the edited image

When I click <b>Cancel</b>
Then I see thumbnails disappear and I see the previous <b>Add</b> or <b>Edit</b> article page without changes

When I click the crop icon
Then I see a frame over the image with four control points on each corner of the frame to edit the size in two dimensions. The image outside this frame is covered with a half-transparent overlay

When I capture any control point and pull it
Then I see the picture zone is bordered by frame changes its size

When I click <b>OK</b>
Then I see the image crops to the needed size and is saved

When I click <b>Cancel</b>
Then I see that no changes were applied

When I click the resize icon
Then I see the section for image resizing opens

And I see the resize slider control below the picture box, the <b>Cancel</b> and <b>OK</b> buttons on the right below the picture, and the resize slider control with the small image icon on the left and the bigger image icon on the right

When I pull the slider control to the right
Then I see the picture becomes bigger

When I pull the slider control to the left
Then I see the picture becomes smaller

When I click <b>OK</b>
Then I see the picture is saved with a new size

When I click <b>Cancel</b>
Then I see that no changes were applied

When I click the delete icon
Then I see the picture is deleted and the box for image upload appears
</pre>

## Mockups

1. Admin user hovers over uploaded article image and sees editor actions
2. Admin user clicks a filter icon and sees filters under the article image
3. Admin user clicks a resize icon and sees a size editor
4. Admin user clicks a crop icon and sees a crop editor

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user hovers over uploaded article image and sees editor actions:**

![Admin user hovers over uploaded article image and sees editor actions](/sports_hub_portal/web_application_features/manage_articles/images/article_image_hover_editor.png)

**2. Admin user clicks filter icon and sees filters under the article image:**

![Admin user clicks filter icon and sees filters under the article image](/sports_hub_portal/web_application_features/manage_articles/images/article_image_filters.png)

**3. Admin user clicks resize icon and sees a size editor:**

![Admin user clicks resize icon and sees a size editor](/sports_hub_portal/web_application_features/manage_articles/images/article_image_size_editor.png)

**4. Admin user clicks a crop icon and sees a crop editor:**

![Admin user clicks a crop icon and sees a crop editor](/sports_hub_portal/web_application_features/manage_articles/images/article_image_crop_editor.png)

</details>

## Test cases

1. Verify that admin is able to apply a filter for an article picture
2. Verify that admin is able to cancel the applied filter for an article picture
3. Verify admin is able to crop an article picture
4. Verify admin is able to cancel cropping an article picture
5. Verify admin is able to resize an article picture
6. Verify admin is able to cancel resizing an article picture
7. Verify admin can delete an article picture

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to apply a filter for an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the filters icon</br>4) Select filter</br>5) Click <b>OK</b>|5) The thumbnails disappear and the filter is applied|

### **#2. Verify that admin is able to cancel the applied filter for an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the filters icon</br>4) Select filter</br>5) Click <b>Cancel</b>|5) The thumbnails disappear and no changes are applied to the image|

### **#3. Verify admin is able to crop an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the crop icon</br>4) Capture any control point and pull it</br>5) Click <b>OK</b>|5) The crop editor disappears and the picture is cropped to the proper size and saved|

### **#4. Verify admin is able to cancel cropping an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the crop icon</br>4) Capture any control point and pull it</br>5) Click <b>Cancel</b>|5) The crop editor disappears and no changes are applied to the image|

### **#5. Verify admin is able to resize an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the resize icon</br>4) Move the slider control to the right and to the left</br>5) Click <b>OK</b>|5) The resize editor disappears and the picture is saved with changed size|

### **#6. Verify admin is able to cancel resizing an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the resize icon</br>4) Move the slider control to the right and to the left</br>5) Click <b>Cancel</b>|5) The resize editor disappears and no changes are applied to the image|

### **#7. Verify admin can delete an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the delete icon|4) The image disappears and an empty <b>Picture</b> field is shown|

</details>
