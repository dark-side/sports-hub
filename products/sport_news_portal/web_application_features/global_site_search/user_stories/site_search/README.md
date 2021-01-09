### Back to [Global site search on the portal](../../) feature

# Allow users to use a site search on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to use a site search
    So that I can quickly find the information I am interested in

## Acceptance criteria

<pre>
<b><i>Scenario: A site user uses a site search</i></b>

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
  And enter a search word and click enter
Then I am taken to a search results page

When I view the search results page on the site
And there are no articles found with title or description that matches my search
Then I see "No matches found. Please try another search"

When I view the search results page on the site
  And there are some articles found with the title or description that matches my search
Then I see a page that contains a list of article’s description and a link to the article page with the highlighted search term

When I click on the article from the search results list
Then I am taken to a selected article page
</pre>

## Mockups

1. User sees Search by input at the top of the page
2. User sees a search suggestions list
3. User sees search results
4. Admin User sees search results in CMS

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Search by input at the top of the page:**

![User sees Search by input at the top of the page](/products/sport_news_portal/web_application_features/global_site_search/images/site_search.png)

**2. User sees a search suggestions list:**

![User sees a search suggestions list](/products/sport_news_portal/web_application_features/global_site_search/images/site_search_suggestions.png)

**3. User sees search results:**

![User sees search results](/products/sport_news_portal/web_application_features/global_site_search/images/search_result_in_main_page.png)

**4. Admin User sees search results in CMS:**

![Admin User sees search results in CMS](/products/sport_news_portal/web_application_features/global_site_search/images/search_result_in_cms_page.png)

</details>

## Test cases

1. Verify that the suggestions list is built with proper articles
2. Verify that user is informed that his search term has no matches
3. Verify that user is redirected to the proper article page by click on any article from the Suggestions list
4. Verify that user is redirected to the proper article page by click on any article in the search results list

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the suggestions list is built with proper articles**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- There are only 3 articles in different categories that contain the word **ball**|1) In the page heading, click on the search box, and then enter the word **ball**</br>2) Tap **Enter**|1) Suggestions list is formed only with 3 articles that contain the word **ball**</br>2) Search results page contains only 3 articles that contain the word **ball**|

### **#2. Verify that user is informed that his search term has no matches**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- There are no articles in different categories that contain the word **ball**|1) In the page heading, click on the search box, and then enter the word **ball**</br>2) Tap **Enter**|1) No suggestions are shown</br>2) "No matches found. Please try another search" message appears on the search results page|

### **#3. Verify that user is redirected to the proper article page by click on any article from the Suggestions list**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to Sport News home page|1) In the page heading, click on the search box, and then enter some words</br>2) Click on any article from the suggestions list|1) The search term is highlighted in search results</br>2) User is redirected to the proper article page|

### **#4. Verify that user is redirected to the proper article page by click on any article in the search results list**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to Sport News home page</br>- User is logged in|1) In the page heading, click on the search box, and then enter some words</br>2) Tap Enter</br>3) Click on any article from the suggestions list|1) The search term is highlighted in search results</br>2) User is redirected to the proper article page|
</details>
