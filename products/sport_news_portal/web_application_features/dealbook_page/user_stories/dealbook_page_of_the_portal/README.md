### Back to [Dealbook Page of the portal](/../../) feature

# Allow users to view a dealbook page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to open the Dealbook page
    So that I can view articles that relate to the financial deals in the sports world

## Acceptance criteria

    Scenario: A user views the Dealbook page
    Given I am logged in as a site user
    
    When I view sidebar menu
    Then I see a Dealbook menu item right after the Lifestyle menu item
    When I click on the Dealbook menu item
    Then I am redirected to Dealbook page
    When I view a Dealbook page 
    Then I see: 
      - Heading “Dealbook” at the top of the page
      - Big photo from the most recent article in the Dealbook category with the square on the right side of the photo that contains:
        - Article headline
        - Article metadata (including author and source)
        - More button in the left-bottom corner
      - The list of articles (the number of articles to show can be specified in the CMS) located below the photo from the most recent article including: 
        - Article thumbnail photo in the left side
        - Article Headline to the right from the photo
        - First few sentences of the article content 
      - Scroll bar next to the list of articles
    When I click on any article or click on More button
    Then I am taken to the page containing the article
    When I scroll the list of the articles
    Then I see a list of articles is appended with a new portion of articles 
    And I see the list of articles should be relevant to the Dealbook topics
    And I see the number of articles that appear in the list should be defined in the CMS

## Mockups
1. User sees Dealbook page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Dealbook page:**

![Dealbook page Screen](/products/sport_news_portal/web_application_features/dealbook_page/images/dealbook_page.png)

</details>

## Test Scenarios

1. Verify redirecting Dealbook page
2. Verify Dealbook page content
3. Verify the content of an article from the list on Dealbook page
4. Verify clicking on an article from the list on Dealbook page
5. Verify scrolling the list of articles

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify redirecting Dealbook page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The Dealbook menu item is situated right after the More menu item
|4|Click on Dealbook menu item|User is redirected to Dealbook page

### **#2. Verify Dealbook page content**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The Dealbook menu item is situated right after the More menu item
|4|Click on Dealbook menu item|User is redirected to Dealbook page
|5|Examine the content of the Dealbook page|The Dealbook page consists of:<br>- Heading “Dealbook” at the top of the page<br>- Big photo from the most recent article in the Dealbook category with article headline and article metadata (including author and source) in the square on the right side of the photo<br>- The list of 5 articles (below the photo from the most recent article)<br>- Scroll bar next to the list of articles

### **#3. Verify the content of an article from the list on Dealbook page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The Dealbook menu item is situated right after the More menu item
|4|Click on Dealbook menu item|User is redirected to Dealbook page
|5|Examine the content of an article on Dealbook page|The list of 5 articles includes:<br>- Article thumbnail photo in the left side<br>- Article Headline to the right from the photo<br>- First few sentences of the article content 

### **#4. Verify clicking on an article from the list on Dealbook page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The Dealbook menu item is situated right after the More menu item
|4|Click on Dealbook menu item|User is redirected to Dealbook page
|5|Click on an article from the list on Dealbook page|User is taken to the page containing the article

### **#5. Verify scrolling the list of articles**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe a scroll bar|The Dealbook menu item is situated right after the More menu item
|4|Click on Dealbook menu item|User is redirected to Dealbook page
|5|Scroll the list of articles|The list of articles is appended with a new portion of articles and the list of articles should be relevant to the Lifestyle topics

</details>
