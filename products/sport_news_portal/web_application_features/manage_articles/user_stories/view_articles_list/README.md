### Back to [Manage Articles of the portal](/../../) feature

# Allow admin users to view the list of existing articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to view the list of existing articles

## Acceptance criteria

    Scenario: An admin user views the list of existing articles
    Given I am logged in as an admin user

    When I click any sports category link on the admin side 
    Then I see the next elements:
      - +New Article button in the top-right corner of the screen
      - The list of blocks – one block per one of the existing articles from the selected category – where each block has:
        - Article thumbnail photo in the left side
        - Article Headline to the right from the photo
        - First few sentences of the article content
      - The "Conference" and "Teams" dropdowns above the list of the articles with All value by default 
      - The scroll bar next to the list of articles
    When I click on the +New Article button
    Then I am redirected to Create Article page
    When I scroll the list of the articles
    Then I see a list of articles is appended with a new portion of articles
    When I change the "Conference" value
    Then I see available values in the "Teams" dropdown is refreshed 
      And I see list of articles is refreshed
      And I see articles that relate to selected conference
    When I change the "Teams" value
    Then I see the list of articles is refreshed
      And I see articles that relate to the selected team
    When I hover the article
    Then I see the overflow menu icon in the top-right corner
    When I click on the menu icon
    Then I see the next options:
      - Unpublish if the article is published or Publish if the article is unpublished
      - Edit
      - Delete
      - Move
    When I hover Move option
    Then I see another dropdown menu with the list of sports categories
    When I click on another sport category
    Then I see the category of the article is changed to the selected one and Conference & Team of that article reset
    When I click Unpublish/Publish option
    Then I see the article becomes hidden/visible for the regular user

## Mockups

1. User sees list of articles
2. User sees move article option
3. User sees article is published popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees list of articles:**

![Articles list Screen](/products/sport_news_portal/web_application_features/manage_articles/images/articles_list.png)

**2. User sees move article option:**

![Move article dropdown Screen](/products/sport_news_portal/web_application_features/manage_articles/images/move_article.png)

**3. User sees article is published popup:**

![Article is published popup](/products/sport_news_portal/web_application_features/manage_articles/images/publish_article_popup.png)

</details>

## Test Scenarios

1. Verify the content of a sport category page from the admin side
2. Verify click on the +New Article button
3. Verify that admin is able to scroll the list of the articles
4. Verify that admin is able to change the "Conference" value
5. Verify content of overflow menu of the article
6. Verify move option dropdown
7. Verify changing sport category in move option dropdown
8. Verify clicking on Unpublish/Publish option

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of a sport category page from the admin side**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Observe the content of a sport category page from the admin side|- +New Article button in the top-right corner of the screen<br>- The "Conference" and "Teams" dropdowns above the list of the articles with All value by default<br>- The scroll bar next to the list of articles<br>- The list of blocks – one block per one of the existing articles from the selected category – where each block has:<br><ul><li>Article thumbnail photo in the left side</li><li>Article Headline to the right from the photo</li><li>First few sentences of the article content</li></ul>

### **#2. Verify click on the +New Article button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|
|4|Click on +New Article button|Admin is redirected to Create Article page

### **#3. Verify that admin is able to scroll the list of the articles**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Scroll the list of the articles|Admin is able to scroll the articles and the list of articles is appended with a new portion of articles

### **#4. Verify that admin is able to change the "Conference" value**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Click on All Conference dropdown|"Teams" dropdown appears
|5|Choose the team|The list of articles is refreshed and articles that relate to selected conference are shown

### **#5. Verify content of overflow menu of the article**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|Overflow menu appears
|6|Check what options are there|The next options should be present:<br>- Unpublish if the article is published or Publish if the article is unpublished<br>- Edit<br>- Delete<br>- Move

### **#6. Verify move option dropdown**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|Overflow menu appears
|6|Hover Move option|Another dropdown menu with the list of sports categories appears

### **#7. Verify changing sport category in move option dropdown**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|Overflow menu appears
|6|Hover Move option|Another dropdown menu with the list of sports categories appears
|7|Click on sport category from dropdown|The category of the article will be changed to the selected one and Conference & Team of that article will be reset

### **#8. Verify clicking on Unpublish/Publish option**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|Overflow menu appears
|6|Click on Unpublish/Publish option|The article becomes hidden/visible for the regular user

</details>

