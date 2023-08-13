### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to see a list of news from partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to see a list of news from partners

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is viewing the partners articles list page</i></b>

Given I am logged in as an admin user

When I view the <b>News Partners</b> page
Then I see the following:
  - Page headline in the upper-left corner
  - <b>Partners</b> tab is active
  - <b>News</b> tab
  - Empty state message that informs about the absence of integrations with partners

When I click <b>News</b> tab
Then I see a list of articles from the partners
  And the list consists of blocks – one block per one existing article:
    - Article thumbnail photo on the left side
    - Article headline on the right from the photo
    - Article status (can be:
      - <b>Draft</b> - black color
      - <b>Ready for processing</b> - blue color
      - <b>Processing</b> - yellow color
      - <b>Processed</b> - green color)
    - First few sentences of the article
    - Category and team names below the article text
    - A green circle indicates the <b>Published</b> status of the article

When I hover over an article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner
  And the ellipsis (<b>...</b>) button is available only for <b>Draft</b> articles

When I click the "<b>...</b>" menu icon
Then I see the following options:
  - <b>Edit</b>
  - <b>Delete</b>
  - <b>Ready for processing</b>

When I scroll the list of the articles
Then I see the pagination
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees articles list
2. Admin user hovers over the article and sees the ellipsis (<b>...</b>) button
3. Admin user hovers over the article, clicks the ellipsis (<b>...</b>) button, and sees action list

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees articles list:**

![Admin user sees articles list](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_side_partner_articles_list.png)

**2. Admin user hovers over the article and sees the ellipsis (...) button:**

![Admin user hovers over the article and sees the ellipsis (...) button](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_hovers_over_article.png)

**3. Admin user hovers over the article, clicks the ellipsis (...) button, and sees action list:**

![Admin user hovers over the article, clicks the ellipsis (...) button, and sees action list](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_clicks_ellipsis_button.png)

</details>

## Test cases

1. Verify that the list of articles from the news partner shown on the <b>News</b> tab
2. Verify that the the pagination works on the <b>News</b> tab of the <b>News Partners</b> page
3. Verify the ellipsis (...) button is visible on hover over the draft article
4. Verify the expected list is visible when the admin user clicks the ellipsis (...) button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the list of articles from the news partner shown on the News tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Examine the articles list|3) Each news is displayed as a block with the next elements:</br>- Article thumbnail photo on the left side</br>- Article headline on the right from the photo</br>- Article status</br>- First few sentences of the article</br>- Category and team names below the article text</br>- A green circle indicates the <b>Published</b> status of the article</br></br>And the possible statuses are rendered in expected colors:</br>- <b>Draft</b> - black color</br>- <b>Ready for processing</b> - blue color</br>- <b>Processing</b> - yellow color</br>- <b>Processed</b> - green color|

### **#2. Verify that the the pagination works on the News tab of the News Partners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Examine the bottom of the articles list</br>4) Click any page on the pagination|3) The pagination is present</br>4) The artile list is updated|

### **#3. Verify the ellipsis (...) button is visible on hover over the draft article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have a draft arcticle</br>4) Hover over the draft article</br>5) Have a ready for processing arcticle</br>6) Hover over the ready for processing arcticle|4) The ellipsis (...) button is visible</br>6) The ellipsis (...) button is not visible|

### **#4. Verify the expected list is visible when the admin user clicks the ellipsis (...) button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have a draft arcticle</br>4) Hover over the draft article</br>5) Click the ellipsis (...) button|4) The ellipsis (...) button is visible</br>5) The next options are visible: <b>Edit</b>, <b>Delete</b>, <b>Ready for processing</b>|
</details>
