### Back to [Lifestyle and Dealbook news](../../README.md) feature

# Allow admin users to view the list of existing articles in Lifestyle and Dealbook

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the list of existing articles in Lifestyle and Dealbook

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the list of existing articles in Lifestyle and Dealbook</i></b>

Given I am logged in as an admin user

When I select the <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the <b>+ New Article</b> button in the upper-right corner of the page

Then I see the following:
  - The <b>+ New Article</b> button in the upper-right corner of the page
  - A preview icon
  - A filter by status
  - A search icon
  - The list of blocks – one block per one existing article – where each block has:
    - Article thumbnail photo on the left side
    - Article headline on the right of the photo
    - First few sentences of the article
  - Status of the article (<b>Published</b> or <b>Unpublished</b>)
  - The scroll bar next to the list of articles

When I scroll the list of the articles
Then I see a list of articles is appended with a new portion of articles

When I select a <b>Published</b> option in the status filter
Then I see only published articles

When I select an <b>Unpublished</b> option in the status filter
Then I see only unpublished articles

When I select <b>All</b> option in the status filter
Then I see all articles

When I click a search icon
Then I see a search field

When I type some text in the field
Then I see the list of articles is refreshed with matching results
(<i>Search can start when the first symbol is entered or when at least 3 symbols are entered</i>)

When I click a preview icon
Then I see how <b>Lifestyle</b> or <b>Dealbook</b> category is shown for users
  And I see <b>Back to admin page</b> link

When I select <b>Back to admin page</b> link
Then I am taken back to <b>Lifestyle</b> or <b>Dealbook</b> admin page

When I hover over an article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" button
Then I see the following options:
  - <b>Unpublish</b> if the article is published or <b>Publish</b> if the article is unpublished
  - <b>Edit</b>
  - <b>Delete</b>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees a <b>Lifestyle</b> list of articles
2. Admin user sees a <b>Dealbook</b> list of articles
3. Admin user sees actions for a published article on <b>Dealbook</b> and <b>Lifestyle</b> configuration pages
4. Admin user clicks status filter and sees the options
5. Admin user clicks a search icon and sees an input field
6. Admin user sees the <b>Lifestyle</b> preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a Lifestyle list of articles:**

![Admin user sees a Lifestyle list of articles](/sports_hub_portal/desktop_application_features/lifestyle_dealbook_news/images/lifestyle_index_page.png)

**2. Admin user sees a Dealbook list of articles:**

![Admin user sees a Dealbook list of articles](/sports_hub_portal/desktop_application_features/lifestyle_dealbook_news/images/dealbook_index_page.png)

**3. Admin user sees actions for a published article on Dealbook and Lifestyle configuration pages:**

![Admin user sees actions for a published article on Dealbook and Lifestyle configuration pages](/sports_hub_portal/desktop_application_features/lifestyle_dealbook_news/images/article_actions_index_page.png)

**4. Admin user clicks status filter and sees the options:**

![Admin user clicks status filter and sees the options](/sports_hub_portal/desktop_application_features/lifestyle_dealbook_news/images/status_filter_options.png)

**5. Admin user clicks a search icon and sees an input field:**

![Admin user clicks a search icon and sees an input field](/sports_hub_portal/desktop_application_features/lifestyle_dealbook_news/images/search_field.png)

**6. Admin user sees the Lifestyle preview page:**

![Admin user sees the Lifestyle preview page](/sports_hub_portal/desktop_application_features/lifestyle_dealbook_news/images/lifestyle_preview_page.png)

</details>

## Test cases

1. Verify the content of the <b>Lifestyle</b> and <b>Dealbook</b> index pages
2. Verify that list of articles is populated with new elements when it is scrolled down
3. Verify that list of articles is updated according to the selected status filter
4. Verify that list of articles is updated according to a search match

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Lifestyle and Dealbook index pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b>|1) Examine the index pages for <b>Lifestyle</b> and <b>Dealbook</b>|1) There are blocks of articles where each block has:</br>- Article thumbnail photo on the left side</br>- Article headline on the right of the photo</br>- First few sentences of the article</br>- Status of the article (<b>Published/Unpublished</b>)|

### **#2. Verify that list of articles is populated with new elements when it is scrolled down**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There are a lot of articles to load|1) Move through the list of articles</br>2) Check if the articles list is loaded|2) When an admin moves through the list of articles, the articles are loaded|

### **#3. Verify that list of articles is updated according to the selected status filter**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There are a lot of articles to load|1) In the status filter, select the <b>Published</b> option</br>2) Check if the list with articles is updated</br>3) In the status filter, select the <b>Unpublished</b> option</br>4) Check if the list with articles is updated</br>5) In the status filter, select the <b>All</b> option</br>6) Check if the list with articles is updated|2) Only published articles are shown</br>4) Only unpublished articles are shown</br>6) All articles are shown|

### **#4. Verify that list of articles is updated according to a search match**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There are a lot of articles to load|1) Click a search icon</br>2) Type some text to the field|1) An input field appears</br>2) The list of articles is updated with match|

</details>
