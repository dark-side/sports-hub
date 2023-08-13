### Back to [Global site search on the portal](../../README.md) feature

# Allow users to use site search on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to use site search
    So that I can quickly find the information I am interested in

## Acceptance criteria

<pre>
<b><i>Scenario: A site user uses site search</i></b>

Given I am a site user

When I view any page on the site
Then I see the <b>Search by</b> field in the page header

When I click the search field and enter words
Then I see the list with articles matching my search

When I select an article from the suggestions list
Then I am taken to the selected article page

When there is no article matching my search
Then I don’t see the suggestions list

When I don’t select any item from the suggestions list
  And enter a search word and click <b>Enter</b>
Then I am taken to the search results page

When I view the search results page on the site
And there are no articles found with title or description that matches my search
Then I see "No matches found. Please try another search"

When I view the search results page on the site
  And there are some articles found with the title or description that matches my search
Then I see a page that contains a list of article’s description and a link to the article page with the highlighted search term

When I select the article from the search results list
Then I am taken to the selected article page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Search by</b> input at the top of the page
2. Users see a search suggestions list
3. Users see search results
4. Admin user sees search results in CMS

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Search by input at the top of the page:**

![Users see Search by input at the top of the page](/web_application_features/global_site_search/images/site_search.png)

**2. Users see a search suggestions list:**

![Users see a search suggestions list](/web_application_features/global_site_search/images/site_search_suggestions.png)

**3. Users see search results:**

![Users see search results](/web_application_features/global_site_search/images/search_result_in_main_page.png)

**4. Admin user sees search results in CMS:**

![Admin user sees search results in CMS](/web_application_features/global_site_search/images/search_result_in_cms_page.png)

</details>

## Test cases

1. Verify that the suggestions list is built with proper articles
2. Verify that users are informed that their search term has no matches
3. Verify that users are redirected to the proper article page by selecting any article from the suggestions list
4. Verify that users are redirected to the proper article page by selecting any article in the search results list

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the suggestions list is built with proper articles**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- There are only 3 articles in different categories that contain the word **ball**|1) In the page heading, select the search box, and then enter the word **ball**</br>2) Click **Enter**|1) Suggestions list is formed only with 3 articles that contain the word **ball**</br>2) Search results page contains only 3 articles that contain the word **ball**|

### **#2. Verify that users are informed that their search term has no matches**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- There are no articles in different categories that contain the word **ball**|1) In the page heading, select the search box, and then enter the word **ball**</br>2) Click **Enter**|1) No suggestions are shown</br>2) "No matches found. Please try another search" message appears on the search results page|

### **#3. Verify that users are redirected to the proper article page by selecting any article from the suggestions list**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to the Sports Hub home page|1) In the page heading, select the search box, and then enter some words</br>2) Select any article from the suggestions list|1) The search term is highlighted in search results</br>2) The user is redirected to the proper article page|

### **#4. Verify that users are redirected to the proper article page by selecting any article in the search results list**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- The user is logged in|1) In the page heading, select the search box, and then enter some words</br>2) Click **Enter**</br>3) Select any article from the suggestions list|1) The search term is highlighted in search results</br>2) The user is redirected to the proper article page|
</details>
