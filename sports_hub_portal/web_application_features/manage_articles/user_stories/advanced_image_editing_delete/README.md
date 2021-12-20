### Back to [Manage articles on the portal](../../) feature

# Allow admin users to have advanced editor of the article image - image deletion

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have an editor function that allows to delete the picture

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes an image of an article</i></b>

Given I am logged in as an admin user

When I hover over the <b>Picture</b> box on the <b>Add</b> or <b>Edit</b> article page
Then I see the delete picture icon

When I click the delete icon
Then I see the picture is deleted and the box for image upload appears
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user hovers over uploaded article image and sees a delete icon

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user hovers over uploaded article image and sees a delete icon:**

![Admin user hovers over uploaded article image and sees a delete icon](/sports_hub_portal/web_application_features/manage_articles/images/article_image_hover_editor.png)
</details>

## Test cases

1. Verify admin can delete an article picture

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify admin can delete an article picture**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page|1) Click <b>+Add Article</b></br>2) Upload some picture</br>3) In the <b>Picture</b> section, click the delete icon|4) The image disappears and an empty <b>Picture</b> field is shown|

</details>
