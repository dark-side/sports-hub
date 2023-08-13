### Back to [Manage articles on the portal](../../README.md) feature

# Allow admin users to have advanced editor of the article image - image update

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have an editor function that allows to update the picture

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits and updates an image of an article</i></b>

Given I am logged in as an admin user

When I hover over the <b>Picture</b> box on the <b>Add</b> or <b>Edit</b> article page
Then I see the Upload new image icon

When I click the Upload new image icon
Then I see a window to select an image and can select only supported formats (PNG, JPG, JPEG, TIF)

When I select and image of supported formats
Then the article image is updated
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user hovers over uploaded article image and sees upload new image icon

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user hovers over uploaded article image and sees upload new image icon:**

![Admin user hovers over uploaded article image and sees upload new image icon](/desktop_application_features/manage_articles/images/article_image_hover_editor.png)

</details>

## Test cases

1. Verify that admin is able to upload new article picture

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to apply a filter for an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the upload new image icon</br>4) Select a new image</br>5) Click <b>OK</b>|5) The new image appears|

</details>
