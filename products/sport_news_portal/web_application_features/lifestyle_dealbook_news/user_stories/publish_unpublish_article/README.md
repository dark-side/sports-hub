### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to publish/unpublish Lifestyle and Dealbook's articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to publish/unpublish existing articles in Lifestyle and Dealbook

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user publishes/unpublishes an existing article</i></b>

Given I am logged in as an admin user

When I select <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the list of blocks with articles

When I hover over any article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an unpublished article
Then I see the <b>Publish</b> menu item present

When I click <b>Publish</b> menu item
Then I see a success message
  And the status of article changed to <b>Published</b>
  And article is visible for users in <b>Lifestyle</b> and <b>Dealbook</b>

When I click "<b>...</b>" the menu icon for a published article
Then I see the <b>Unpublish</b> menu item present

When I click <b>Unpublish</b> menu item
Then I see a success message
  And the status of article changed to <b>Unpublished</b>
  And article is not visible for users anymore
</pre>

## Mockups

1. Admin user sees article actions on <b>Dealbook</b> and <b>Lifestyle</b> index pages

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees article actions on Dealbook and Lifestyle index pages:**

![Admin user sees article actions on Dealbook and Lifestyle index pages](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/article_actions_index_page.png)

</details>

## Test cases

1. Verify that admin is able to publish an existing unpublished article
2. Verify that admin is able to unpublish an existing published article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to publish an existing unpublished article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Publish</b> menu item|2) A success message appears and users can see the article|

### **#2. Verify that admin is able to unpublish an existing published article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is a published article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Unpublish</b> menu item|2) A success message appears and users do not see the article|
</details>
