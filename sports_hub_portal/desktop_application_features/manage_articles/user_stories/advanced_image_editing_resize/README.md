### Back to [Manage articles on the portal](../../README.md) feature

# Allow admin users to have advanced editor of the article image - image resize

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have an editor function that allows to resize the picture

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits and resizes an image of an article</i></b>

Given I am logged in as an admin user

When I hover over the <b>Picture</b> box on the <b>Add</b> or <b>Edit</b> article page
Then I see the resize icon

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
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user hovers over uploaded article image and sees a resize icon
2. Admin user clicks a resize icon and sees a size editor

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user hovers over uploaded article image and sees a resize icon:**

![Admin user hovers over uploaded article image and sees a resize icon](/sports_hub_portal/desktop_application_features/manage_articles/images/article_image_hover_editor.png)

**2. Admin user clicks resize icon and sees a size editor:**

![Admin user clicks resize icon and sees a size editor](/sports_hub_portal/desktop_application_features/manage_articles/images/article_image_size_editor.png)

</details>

## Test cases

1. Verify admin is able to resize an article picture
2. Verify admin is able to cancel resizing an article picture

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify admin is able to resize an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the resize icon</br>4) Move the slider control to the right and to the left</br>5) Click <b>OK</b>|5) The resize editor disappears and the picture is saved with changed size|

### **#2. Verify admin is able to cancel resizing an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the resize icon</br>4) Move the slider control to the right and to the left</br>5) Click <b>Cancel</b>|5) The resize editor disappears and no changes are applied to the image|
</details>
