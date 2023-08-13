### Back to [Manage articles on the portal](../../README.md) feature

# Allow admin users to move an existing article between categories

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to move an existing article between categories

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user moves an existing article between categories</i></b>

Given I am logged in as an admin user

When I select any sports category link on the admin side
Then I see the list of blocks with articles

When I hover over an article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an article
Then I see the <b>Move</b> menu item present

When I select <b>Move</b> menu item
Then I see the list of available categories except the current one

When I select any category
Then I see the "The article is successfully moved" flash message
  And the article is not present in the current category

When I go to the category where the article is moved
Then I see the article is present
  And the <b>Subcategory</b> and <b>Team</b> are reset for the article
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>Move</b> among actions for the article

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Move among actions for the article:**

![Admin user sees Move among actions for the article](/sports_hub_portal/web_application_features/manage_articles/images/published_article_actions.png)

</details>

## Test cases

1. Verify that admin is able to move an unpublished article to another category
2. Verify that admin is able to move a published article to another category

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to move an unpublished article to another category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Move</b> menu item</br>3) Select any category</br>4) Examine the list of articles in the current category</br>5) Go to the category selected in step 3</br>6) Examine the list of articles|3) "The article is successfully moved" flash message appears</br>4) Article is not present in the current list</br>6) Article is present in the list in the <b>Unpublished</b> state. <b>Subcategory</b> and <b>Team</b> are reset for the article in case of any|

### **#2. Verify that admin is able to move a published article to another category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is a published article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Move</b> menu item</br>3) Select any category</br>4) Examine the list of articles in the current category</br>5) Go to the category selected in step 3</br>6) Examine the list of articles|3) "The article is successfully moved" flash message appears</br>4) Article is not present in the current list</br>6) Article is present in the list in the <b>Published</b> state. <b>Subcategory</b> and <b>Team</b> are reset for the article in case of any|

</details>
