### Back to [Global site search on the portal](../../) feature

# Allow users to use a site search on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to use a site search  
    So that I can quickly find the information I’m interested in

## Acceptance criteria

    Scenario: A site user uses a site search
    Given I am logged in as a site user

    When I view any page on the site 
    Then I see a Search by input at the top of the page 
    When click on the Search By input and enter some search term
    Then I see a search suggestions list with list of articles matching my search term
    When I select any article from the suggestions list 
    Then I am taken to the selected article page
    When there is no article found matching my search term
    Then I don’t see a suggestions list
    When I don’t select any item from the suggestions list
    But enter a search term and click enter,
    Then I am taken to a search results page
    When I view a search results page on the site 
      And there is no articles found with title or description that matches my search term 
    Then I see a “No matches found. Please try another search” message
    When I view a search results page on the site 
      And there are some articles found with title or description that matches my search term 
    Then I see a page that contains a list of article’s description and a link to the article page with the highlighted search term
    When I click on the article from the search results list 
    Then I am taken to a selected article page

## Mockups

1. User sees Search by input at the top of the page 
2. User sees a search suggestions list
3. User sees search results
4. Admin User sees search results in CMS

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Search by input at the top of the page:**

![CSearch by input](/products/sport_news_portal/web_application_features/global_site_search/images/site_search.png)

**2. User sees a search suggestions list:**

![Search suggestions list](/products/sport_news_portal/web_application_features/global_site_search/images/site_search_suggestions.png)

**3. User sees search results:**

![Search results](/products/sport_news_portal/web_application_features/global_site_search/images/search_result_in_main_page.png)

**4. Admin User sees search results in CMS:**

![Search results in CMS](/products/sport_news_portal/web_application_features/global_site_search/images/search_result_in_cms_page.png)

</details>

## Test Scenarios

1. Verify that admin can click on search By input
2. Verify search suggestions in the Site Menu
3. Verify selecting any article from the suggestions list
4. Verify redirecting to search result page
5. Verify articles that matches the search term
6. Verify clicking on the article from the search results list

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can click on search By input**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe the Search By input|A Search By input is situated at the top of the page

### **#2. Verify search suggestions in the Site Menu**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Click on the Search By input|A search suggestions with a list of articles available in the Site Menu appears

### **#3. Verify selecting any article from the suggestions list**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Click on the Search By input|A search suggestions with a list of articles available in the Site Menu appears
|4|Select any article from the suggestions list|The system redirects user to a selected articles page

### **#4. Verify redirecting to search result page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Click on the Search By input|
|4|Don’t select any article from the suggestions list|
|5|Click Enter|The system redirects me to a search results page

### **#5. Verify articles that matches the search term**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport site news|
|2|Log in to the user account|
|3|Сlick on the Search By input|
|4|Type some search term|There are some articles found with title or description that matches my search term

### **#6. Verify clicking on the article from the search results list**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport site news|
|2|Log in to the user account|
|3|Click on Search By input at the top of the page| 
|4|Don’t select any league/team from the suggestions list, but enter a search term and click enter|
|5|Observe search result page|Page that contains a list of article’s description and a link to the article page with the highlighted search term
|6|Click on any link to article from the search results list|User is redirected to a selected article page

</details>
