### Back to [Global application search](../../README.md) feature

# Allow users to use application search

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to use search
    So that I can quickly find the information I am interested in

## Acceptance criteria

<pre>
<b><i>Scenario: A user uses search</i></b>

Given I am an user

When I view any page
Then I see the Search icon at the top of the page

When I tap the search icon and enter words
Then I see the list with articles matching my search

When I select an article from the suggestions list
Then I am taken to the selected article page

When there is no article matching my search
Then I see "No matches found. Please try another search" message

When I cancel search and tap search icon again
Then I see a list of my recent searches
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Search</b> icon at the top of the page
2. Users see a search suggestions list
3. Users see recent search results

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Search icon at the top of the page:**

![Users see Search icon at the top of the page](/mobile_application_features/global_application_search/images/application_search_icon.png)

**2. Users see a search suggestions list:**

![Users see a search suggestions list](/mobile_application_features/global_application_search/images/application_search_suggestions.png)

**3. Users see recent search results:**

![Users see recent search results](/mobile_application_features/global_application_search/images/application_recent_search.png)

</details>

## Test cases

1. Verify that the suggestions list is built with proper articles
2. Verify that users are informed that their search term has no matches
3. Verify that users are redirected to the proper article page by tapping any article from the suggestions list
4. Verify that users see recent searches

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the suggestions list is built with proper articles**

|Preconditions|Steps|Expected result
------|-------|----------
|- There are only 3 articles in different categories that contain the word ball|1) In the page heading, tap the search icon, and then enter the word ball</br>2) Tap Enter|1) Suggestions list is formed only with 3 articles that contain the word ball</br>2) Search results page contains only 3 articles that contain the word ball|

### **#2. Verify that users are informed that their search term has no matches**

|Preconditions|Steps|Expected result
------|-------|----------
|- There are no articles in different categories that contain the word ball|1) In the page heading, tap the search icon, and then enter the word <b>ball</b></br>2) Tap Enter|1) No suggestions are shown</br>2) "No matches found. Please try another search" message appears|

### **#3. Verify that users are redirected to the proper article page by tapping any article from the suggestions list**

|Preconditions|Steps|Expected result
------|-------|----------
||1) In the page heading, tap the search icon, and then enter some words</br>2) Select any article from the suggestions list|1) The search term is highlighted in search results</br>2) The user is redirected to the proper article page|

### **#4. Verify that users see recent searches**

|Preconditions|Steps|Expected result
------|-------|----------
|- User did some searches|1) In the page heading, tap on the search icon|1) The recent searches are displayed|
</details>
