### Back to [Lifestyle – Sidebar Block](../../) feature

# Allow users to view Lifestyle page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to open the Lifestyle page
    So that I can view articles that relate to the daily life of sports celebrities

## Acceptance criteria

    Scenario: A site user views articles that relate to the Lifestyle page
    Given I am logged in as a site user

    When I view sidebar menu
    Then I see the Lifestyle menu item right after the More menu item
    When I click on the Lifestyle menu item
    Then I am redirected to Lifestyle page
    When I view a Lifestyle page 
    Then I see: 
      - Heading “Lifestyle” at the top of the page
      - Big photo from the most recent article in the lifestyle category with the square on the right side of the photo that contains:
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
      And I see the list of articles should be relevant to the Lifestyle topics
      And I see the number of articles that appear in the list should be defined in the CMS

## Mockups

1. User sees Lifestyle page 

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Lifestyle page:**

![Lifestyle Screen](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/images/lifestyle.png)

</details>

## Test Scenarios

1. Verify redirecting Lifestyle page
2. Verify Lifestyle page content
3. Verify the content of an article from the list on Lifestyle page
4. Verify clicking on an article from the list on Lifestyle page
5. Verify scrolling the list of articles

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify redirecting Lifestyle page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The lifestyle menu item is situated right after the More menu item
|4|Click on Lifestyle menu item|User is redirected to Lifestyle page

### **#2. Verify Lifestyle page content**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The lifestyle menu item is situated right after the More menu item
|4|Click on Lifestyle menu item|User is redirected to Lifestyle page
|5|Examine the content of the Lifestyle page|The Lifestyle page consists of:<br> - Heading “Lifestyle” at the top of the page<br> - Big photo from the most recent article in the lifestyle category with article headline and article metadata (including author and source) in the square on the right side of the photo<br> - The list of 5 articles (below the photo from the most recent article)<br> - Scroll bar next to the list of articles

### **#3. Verify the content of an article from the list on Lifestyle page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The lifestyle menu item is situated right after the More menu item
|4|Click on Lifestyle menu item|User is redirected to Lifestyle page
|5|Examine the content of an article on Lifestyle page|The list of 5 articles includes:<br> - Article thumbnail photo in the left side<br> - Article Headline to the right from the photo<br> - First few sentences of the article content

### **#4. Verify clicking on an article from the list on Lifestyle page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|The lifestyle menu item is situated right after the More menu item
|4|Click on Lifestyle menu item|User is redirected to Lifestyle page
|5|Click on an article from the list on Lifestyle page|User is taken to the page containing the article

### **#5. Verify scrolling the list of articles**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe a scroll bar|The scroll bar is situated next to the list of articles
|4|Click on Lifestyle menu item|User is redirected to Lifestyle page
|5|Scroll the list of the articles|The list of articles will be appended with a new portion of articles and the list of articles should be relevant to the Lifestyle topics

</details>

