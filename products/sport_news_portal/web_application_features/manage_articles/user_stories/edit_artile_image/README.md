### Back to [Manage Articles of the portal](../../) feature

# Allow admin users to edit the image of the article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to edit the image of the article

## Acceptance criteria

    Scenario: An admin user edits the image of the article
    Given I am logged in as an admin user

    When I hover on the field with the image on Add or Edit article page
    Then I see the next elements:
      - link for uploading a new image
      - icon for apply filters
      - icon for crop image
      - icon for deleting the image
      - icon for resizing the image
    When I click Apply filters icon
    Then I see thumbnails with different filter
      And I see the name of each filter above the thumbnails
      And I see OK and Cancel buttons
    When I select the filter
    Then I see the main photo with the applied filter
    When I click OK button
    Then I see thumbnails disappears and I see the previous Add or Edit article page with edited image
    When I click Cancel button
    Then I see thumbnails disappears and I see the previous Add or Edit article page without changes
    When I click the Crop image icon
    Then I see a frame over the image with four control points on each corner of the frame for manipulating with its size in two dimensions. The image outside this frame is covered with half-transparent overlay.
    When I capture any of the control points and pull it
    Then I see the zone bordered by frame changes its size.
    When click Ok button
    Then I see the image crops to the proper size and is saved.
    When I click Cancel button
    Then I see no change and I see the previous Add or Edit article page without changes.
    When I click Resizing icon
    Then I see the section for image resizing opens
      And I see the image on the top, image resize control above and Cancel and Ok buttons on the left bottom corner. Image resize control looks like slider control with two icons on the left and on the right that show small and big image respectively
    When I pull the slider control to the right
    Then I see the image becomes bigger
    When I pull the slider control to the left
    Then I see the image becomes smaller
    When I click Ok button
    Then I see the image is saved with a new size
    When I click Cancel button
    Then I see the previous Add or Edit article page with the edited image.
    When I click Delete icon
    Then I see the image is deleted and form for image upload appears

## Mockups

1. User sees article image
2. User sees crop article image screen
2. User sees edit article image brightness screen
4. User sees apply image filters screen
5. User sees wrong image format popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees article image:**

![Article image Screen](/products/sport_news_portal/web_application_features/manage_articles/images/article_image.png)

**2. User sees crop article image screen:**

![Crop article image Screen](/products/sport_news_portal/web_application_features/manage_articles/images/cancel_edit_article_popup.png)

**3. User sees edit article image brightness screen:**

![Edit article image brightness Screen](/products/sport_news_portal/web_application_features/manage_articles/images/edit_article_image_brightness.png)

**4. User sees apply image filters screen:**

![Apply image filters Screen](/products/sport_news_portal/web_application_features/manage_articles/images/edit_article_filters.png)

**5. User sees wrong image format popup:**

![Wrong image format popup](/products/sport_news_portal/web_application_features/manage_articles/images/wrong_image_format.png)

</details>

## Test Scenarios

1. Verify admin can Apply filter for article photo
2. Verify admin can cancel applied filter for Article image
3. Verify admin can crop an Article image
4. Verify admin can cancel cropping an Article image
5. Verify admin can resize an Article image
6. Verify admin can cancel resizing of an Article image
7. Verify admin can delete an Article image

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify admin can Apply filter for article photo**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on +Add Article button|Admin is navigating to Create Article Page
|5|On the field with the image click on Apply filters icon|Thumbnails with different named filters appears
|6|Select filter|The main photo with the applied filter
|7|Click OK|Thumbnails will disappear and I will see the previous Add article page with edited image

### **#2. Verify admin can cancel applied filter for Article image**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on +Add Article button|Admin is navigating to Create Article Page
|5|On the field with the image click on Apply filters icon|Thumbnails with different named filters appears
|6|Select filter|The main photo with the applied filter
|7|Click Cancel|Thumbnails will disappear and I will see the previous Add article page without changes

### **#3. Verify admin can crop an Article image**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on +Add Article button|Admin is navigating to Create Article Page
|5|On the field with the image click on crop icon|A frame over the image with four control points on each corner of the frame for manipulating with its size in two dimensions appears
|6|Capture any of the control points and pull it|The zone bordered by frame changes its size
|7|Click OK|Image crops to the proper size and is saved

### **#4. Verify admin can cancel cropping an Article image**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on +Add Article button|Admin is navigating to Create Article Page
|5|On the field with the image click on crop icon|A frame over the image with four control points on each corner of the frame for manipulating with its size in two dimensions appears
|6|Capture any of the control points and pull it|The zone bordered by frame changes its size
|7|Click Cancel|Nothing has changed, the Add article page is shown without changes

### **#5. Verify admin can resize an Article image**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on +Add Article button|Admin is navigating to Create Article Page
|5|On the field with the image click on resize icon|Section for image resizing opens
|6|Pull the slider control to the right|The image becomes bigger
|7|Pull the slider control to the left|The image becomes smaller
|8|Click on OK button|The image is saved with a new size

### **#6. Verify admin can cancel resizing of an Article image**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on +Add Article button|Admin is navigating to Create Article Page
|5|On the field with the image click on resize icon|Section for image resizing opens
|6|Pull the slider control to the right|The image becomes bigger
|7|Pull the slider control to the left|The image becomes smaller
|8|Click on Cancel button|The size of Article image has not changed

### **#7. Verify admin can delete an Article image**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Сlick on any sports category link (NBA)|
|4|Click on any article|Admin is redirected to Edit Article page
|5|Click delete on image of the article|Image is deleted and form for image upload appears

</details>

