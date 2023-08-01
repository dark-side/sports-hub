### Back to [Manage articles on the portal](../../) feature

# Allow admin users to view the list of existing articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the list of existing articles per category

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the list of existing articles in the category</i></b>

Given I am logged in as an admin user

When I select any sports category link on the admin side
Then I see the following:
  - The <b>+ New Article</b> button in the upper-right corner of the page
  - The preview icon
  - A drop-down list filtered by statuses (<b>All, Published, Unpublished</b>) with default value <b>All</b>
  - A drop-down list filtered by subcategories with default value <b>All subcategories</b>
  - A drop-down list filtered by teams with default value <b>All teams</b>
  - The search icon
  - The list of blocks – one block per one existing article from the selected category where each block has:
    - Article thumbnail photo on the left side
    - Article headline on the right from the photo
    - First few sentences of the article
    - Category and team names below the article text
    - Status of the article (Published/Unpublished)
  - The scroll bar next to the list of articles

When I scroll the list of the articles
Then I see the list of articles is appended with a new portion of articles

When I select a subcategory in the subcategory drop-down filter
Then I see available items in the team drop-down filter is refreshed
  And I see the list of articles is refreshed
  And I see only articles that are related to selected subcategory

When I select <b>Published</b> option in the status filter
Then I see only published articles

When I select <b>Unpublished</b> option in the status filter
Then I see only unpublished articles

When I select <b>All</b> option in the status filter
Then I see all articles

When I select a team in the team drop-down filter
Then I see the list of articles is refreshed
  And I see only articles that are related to the selected team

When I click the search icon
Then I see the search field

When I type some text in the field
Then I see the list of articles is refreshed with matching results
(<i>Search can start when the first symbol is entered or when at least 3 symbols are entered</i>)

When I click the preview icon
Then I see how this category is shown for the users
  And I see <b>Back to admin page</b> link

When I select <b>Back to admin page</b> link
Then I am taken back to the category admin page

When I hover over an article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click the "<b>...</b>" menu icon
Then I see the following options:
  - <b>Unpublish</b> if the article is published or <b>Publish</b> if the article is unpublished
  - <b>Edit</b> (available only for unpublished articles)
  - <b>Delete</b>
  - <b>Move</b>

<i>You have two options to render a big list: use pagination or infinite scroll</i>

</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees a list of articles
2. Admin user clicks subcategory filter and sees the options
3. Admin user clicks status filter and sees the options
4. Admin user clicks the search icon and sees an input field
5. Admin user sees actions for a published article
6. Admin user sees actions for an unpublished article
7. Admin user sees a category preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a list of articles:**

![Admin user sees a list of articles](/sports_hub_portal/web_application_features/manage_articles/images/articles_list.png)

**2. Admin user clicks subcategory filter and sees the options:**

![Admin user clicks subcategory filter and sees the options](/sports_hub_portal/web_application_features/manage_articles/images/conferences_filter.png)

**3. Admin user clicks status filter and sees the options:**

![Admin user clicks status filter and sees the options](/sports_hub_portal/web_application_features/manage_articles/images/status_filter.png)

**4. Admin user clicks the search icon and sees an input field:**

![Admin user clicks the search icon and sees an input field](/sports_hub_portal/web_application_features/manage_articles/images/search_field.png)

**5. Admin user sees actions for a published article:**

![Admin user sees actions for a published article](/sports_hub_portal/web_application_features/manage_articles/images/published_article_actions.png)

**6. Admin user sees actions for an unpublished article:**

![Admin user sees actions for an unpublished article](/sports_hub_portal/web_application_features/manage_articles/images/unpublished_article_actions.png)

**7. Admin user sees a category preview page:**

![Admin user sees a category preview page](/sports_hub_portal/web_application_features/manage_articles/images/category_preview_page.png)

</details>

## Test cases

1. Verify the content of the category articles page
2. Verify that list of articles is updated according to the selected subcategory in the article subcategory box
3. Verify that list of articles is updated according to the selected team in the article team drop-down filter
4. Verify that list of articles is updated according to the selected status filter
5. Verify that list of articles is populated with new elements when it is scrolled down
6. Verify that list of articles is updated according to a search match

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the category articles page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to any sports category|1) Examine the category articles page|1) There are blocks of articles where each block has:</br>- Article thumbnail photo on the left side</br>- Article headline on the right from the photo</br>- First few sentences of the article</br>- Category/Team below the article text</br>- Status of the article (Published/Unpublished)|

### **#2. Verify that list of articles is updated according to the selected subcategory in the article subcategory box**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to any sports category|1) Select a subcategory in the subcategory drop-down filter</br>2) Check if the list with articles is updated</br>3) Check if the team drop-down filter is updated|2) Articles in the list are updated according to the selected subcategory</br>3) The team drop-down filter is updated according to the selected subcategory|

### **#3. Verify that list of articles is updated according to the selected team in the article team drop-down filter**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to any sports category|1) Select a team in the team drop-down filter</br>2) Check if the list with articles is updated|1) Articles in the list are updated according to the selected team|

### **#4. Verify that list of articles is updated according to the selected status filter**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to any sports category|1) In the status filter, select the <b>Published</b> option</br>2) Check if the list with articles is updated</br>3) In the status filter, select the <b>Unpublished</b> option</br>4) Check if the list with articles is updated</br>5) In the status filter, select the <b>All</b> option</br>6) Check if the list with articles is updated|2) Only published articles are shown</br>4) Only unpublished articles are shown</br>6) All articles are shown|

### **#5. Verify that list of articles is populated with new elements when it is scrolled down**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to any sports category</br>- There are a lot of articles to load|1) Move through the list of articles</br>2) Check if the articles list is loaded|2) When an admin moves through the list of articles, the articles are loaded|

### **#6. Verify that list of articles is updated according to a search match**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to any sports category|1) Click the search icon</br>2) Type some text to the field|1) An input field appears</br>2) The list of articles is updated with match|

</details>
