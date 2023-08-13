### Back to [Manage articles on the portal](../../README.md) feature

# Allow admin users to have advanced editor of the article image - image filters

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to have an editor function that allows to apply filters to the picture

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits an image of an article</i></b>

Given I am logged in as an admin user

When I hover over the <b>Picture</b> box on the <b>Add</b> or <b>Edit</b> article page
Then I see the filters icon

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
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user hovers over uploaded article image and sees filters icon
2. Admin user clicks a filter icon and sees filters under the article image

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user hovers over uploaded article image and sees filters icon:**

![Admin user hovers over uploaded article image and sees filters icon](/web_application_features/manage_articles/images/article_image_hover_editor.png)

**2. Admin user clicks filter icon and sees filters under the article image:**

![Admin user clicks filter icon and sees filters under the article image](/web_application_features/manage_articles/images/article_image_filters.png)

</details>

## Test cases

1. Verify that admin is able to apply a filter for an article picture
2. Verify that admin is able to cancel the applied filter for an article picture

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
</details>
