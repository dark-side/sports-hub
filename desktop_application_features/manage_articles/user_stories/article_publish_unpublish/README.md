### Back to [Manage articles on the portal](../../README.md) feature

# Allow admin users to publish/unpublish an existing article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to publish/unpublish an existing article

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user publishes/unpublishes an existing article</i></b>

Given I am logged in as an admin user

When I select any sports category link on the admin side
Then I see the list of blocks with articles

When I hover over any article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an unpublished article
Then I see the <b>Publish</b> menu item present

When I click <b>Publish</b> menu item
Then I see "The article is successfully published" flash message
  And the status of article changes to <b>Published</b>
  And the article is visible for users in the appropriate category

When I click "<b>...</b>" the menu icon for a published article
Then I see the <b>Unpublish</b> menu item present

When I click <b>Unpublish</b> menu item
Then I see "The article is successfully unpublished" flash message
  And the status of article changed to <b>Unpublished</b>
  And article is not visible for users anymore
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions for a published article
2. Admin user sees actions for an unpublished article

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for a published article:**

![Admin user sees actions for a published article](/desktop_application_features/manage_articles/images/published_article_actions.png)

**2. Admin user sees actions for an unpublished article:**

![Admin user sees actions for an unpublished article](/desktop_application_features/manage_articles/images/unpublished_article_actions.png)

</details>

## Test cases

1. Verify that admin is able to publish an existing unpublished article
2. Verify that admin is able to unpublish an existing published article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to publish an existing unpublished article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Publish</b> menu item|2) "The article is successfully published" flash message appears and the users can see the article|

### **#2. Verify that admin is able to unpublish an existing published article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is a published article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Unpublish</b> menu item|2) "The article is successfully unpublished" flash message appears and the users cannot see the article|

</details>
