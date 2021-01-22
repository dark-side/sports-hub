### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to publish/unpublish Lifestyle and Dealbook's article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to publish/unpublish an existing article in Lifestyle and Dealbook

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user publishes/unpublishes an existing article</i></b>

Given I am logged in as an admin user

When I click <b>Lifestyle/Dealbook</b> link on the admin side
Then I see the list of blocks with articles

When I hover over any article
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." the menu icon for an unpublished article
Then I see the <b>Publish</b> menu item present

When I click <b>Publish</b> menu item
Then I see a success message
  And the status of article changed to <b>Published</b>
  And article is visible for users in <b>Lifestyle/Dealbook</b>

When I click "..." the menu icon for a published article
Then I see the <b>Unpublish</b> menu item present

When I click <b>Unpublish</b> menu item
Then I see a success message
  And the status of article changed to <b>Unpublished</b>
  And article is not visible for users anymore
</pre>

## Mockups

1. Admin user sees article actions on Dealbook and Lifestyle index page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees article actions on Dealbook and Lifestyle index page:**

![Admin user sees article actions on Dealbook and Lifestyle index page](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/article_actions_index_page.png)

</details>

## Test cases

1. Verify that admin is able to Publish an existing unpublished article
2. Verify that admin is able to Unpublish an existing published article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to Publish an existing unpublished article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "..." button -> <b>Publish</b> menu item|2) A success message appears and the users can see the article|

### **#2. Verify that admin is able to Unpublish an existing published article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There is a published article|1) Hover over a published article</br>2) Click "..." button -> <b>Unpublish</b> menu item|2) A success message appears and the users do not see the article|
</details>
