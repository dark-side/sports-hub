### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to view the list of existing articles in Lifestyle and Dealbook

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the list of existing articles in Lifestyle and Dealbook

## Acceptance criteria

<pre>
Scenario: An admin user views the list of existing articles in Lifestyle and Dealbook
Given I am logged in as an admin user

When I click the <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the <b>+ New Article</b> button in the upper-right corner of the page

Then I see the following:
  - <b>+ New Article</b> button in the upper-right corner of the page
  - A preview icon
  - A filter by status
  - A search icon
  - The list of blocks – one block per one existing article – where each block has:
    - Article thumbnail photo on the left side
    - Article headline on the right from the photo
    - First few sentences of the article
  - Status of the article (<b>Published</b> or not)
  - The scroll bar next to the list of articles

When I scroll the list of the articles
Then I see a list of articles is appended with a new portion of articles

When I select a <b>Published</b> option in the status filter
Then I see only published articles

When I select <b>Unpublished</b> option in the status filter
Then I see only unpublished articles

When I select <b>All</b> option in the status filter
Then I see all articles

When I click on a search icon
Then I see a search field

When I type some text in the field
Then I see the list of articles is refreshed with matching results

When I click the preview icon
Then I see how <b>Lifestyle</b>/<b>Dealbook</b> category is shown for the users
  And I see <b>Back to admin page</b> link

When I click <b>Back to admin page</b> link
Then I am taken back to <b>Lifestyle</b> or <b>Dealbook</b> admin page

When I hover over an article
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." button
Then I see the following options:
  - <b>Unpublish</b> if the article is published or <b>Publish</b> if the article is unpublished
  - <b>Edit</b>
  - <b>Delete</b>
</pre>

## Mockups

1. Admin user sees a Lifestyle list of articles
2. Admin user sees a Dealbook list of articles
3. Admin user sees actions for a published article on Dealbook and Lifestyle confiduration page
4. Admin user clicks status filter and sees the options
5. Admin user clicks search icon and sees an input field
6. Admin user sees a Lifestyle preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a Lifestyle list of articles:**

![Admin user sees a Lifestyle list of articles](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/lifestyle_index_page.png)

**2. Admin user sees a Dealbook list of articles:**

![Admin user sees a Dealbook list of articles](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/dealbook_index_page.png)

**3. Admin user sees actions for a published article on Dealbook and Lifestyle confiduration page:**

![Admin user sees actions for a published article on Dealbook and Lifestyle confiduration page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/article_actions_index_page.png)

**4. Admin user clicks status filter and sees the options:**

![Admin user clicks status filter and sees the options](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/status_filter_options.png)

**5. Admin user clicks search icon and sees an input field:**

![Admin user clicks search icon and sees an input field](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/search_field.png)

**6. Admin user sees a Lifestyle preview page:**

![Admin user sees a Lifestyle preview page](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/lifestyle_preview_page.png)

</details>

## Test cases

1. Verify the content of the Lifestyle/Dealbook index pages
2. Verify that list of articles is populated with new elements when it is scrolled down
3. Verify that list of articles is updated according to the selected status filter
4. Verify that list of articles is updated according to a search match

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Lifestyle/Dealbook index pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b>|1) Examine the index pages for Lifestyle and Dealbook|1) There are blocks of articles where each block has:</br>- Article thumbnail photo on the left side</br>- Article Headline on the right from the photo</br>- First few sentences of the article</br>- Status of the article (Published/Unpublished|

### **#2. Verify that list of articles is populated with new elements when it is scrolled down**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There are a lot of articles to load|1) Move through the list of articles</br>2) Check if the articles list is loaded|2) When an admin moves through the list of articles, the articles are loaded|

### **#3. Verify that list of articles is updated according to the selected status filter**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There are a lot of articles to load|1) In the status filter, select the <b>Published</b> option</br>2) Check if the list with articles is updated</br>3) In the status filter, select the <b>Unpublished</b> option</br>4) Check if the list with articles is updated</br>5) In the status filter, select the <b>All</b> option</br>6) Check if the list with articles is updated|2) Only published articles are shown</br>4) Only unpublished articles are shown</br>6) All articles are shown|

### **#4. Verify that list of articles is updated according to a search match**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Lifestyle/Dealbook</b></br>- There are a lot of articles to load|1) Click on a search icon</br>2) Type some text to the field|1) An input field appears</br>2) The list of articles is updated with match|

</details>
