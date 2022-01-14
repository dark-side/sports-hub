### Back to [Manage articles on the portal](../../) feature

# Allow admin users to have advanced editor of the article image - image crop

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have an editor function that allows to crop the picture

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits and crops an image of an article</i></b>

Given I am logged in as an admin user

When I hover over the <b>Picture</b> box on the <b>Add</b> or <b>Edit</b> article page
Then I see the crop picture icon

When I click the crop icon
Then I see a frame over the image with four control points on each corner of the frame to edit the size in two dimensions. The image outside this frame is covered with a half-transparent overlay

When I capture any control point and pull it
Then I see the picture zone is bordered by frame changes its size

When I click <b>OK</b>
Then I see the image crops to the needed size and is saved

When I click <b>Cancel</b>
Then I see that no changes were applied
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user hovers over uploaded article image and sees a crop icon
2. Admin user clicks a crop icon and sees a crop editor

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user hovers over uploaded article image and sees a crop icon:**

![Admin user hovers over uploaded article image and sees a crop icon](/sports_hub_portal/desktop_application_features/manage_articles/images/article_image_hover_editor.png)

**2. Admin user clicks a crop icon and sees a crop editor:**

![Admin user clicks a crop icon and sees a crop editor](/sports_hub_portal/desktop_application_features/manage_articles/images/article_image_crop_editor.png)

</details>

## Test cases

1. Verify admin is able to crop an article picture
2. Verify admin is able to cancel cropping an article picture

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify admin is able to crop an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the crop icon</br>4) Capture any control point and pull it</br>5) Click <b>OK</b>|5) The crop editor disappears and the picture is cropped to the proper size and saved|

### **#2. Verify admin is able to cancel cropping an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the crop icon</br>4) Capture any control point and pull it</br>5) Click <b>Cancel</b>|5) The crop editor disappears and no changes are applied to the image|
</details>
