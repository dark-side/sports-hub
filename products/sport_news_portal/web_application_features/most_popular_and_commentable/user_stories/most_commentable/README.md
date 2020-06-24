### Back to [Most Popular/Commentable articles on the portal](../../) feature

# Allow admin users to view most commentable articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to view a Most Commentable block
    So that I can read articles that have the highest number of comments

## Acceptance criteria

    Scenario: A site user views Most Commentable block
    Given I am logged in as a site user

    When I view a page containing the Most Commentable content block
    Then I see this block with 3 most commentable articles (one below the other)
      And I see for each article:
        - Thumbnail photo
        - Headline (the right from the photo)
        - Caption (under Headline)
    When I click on an article
    Then I am taken to the article page
      And the most commentable block is context-sensitive which means:
        - Home page – contains the most commentable articles from the whole articles list
        - Any other page – contains the most popular and the most commentable articles that belong to a category (or conference or team) of the current page

## Mockups

1. User sees most commentable articles section

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees most commentable articles section:**

![Screen with Popular/Commentable section](/products/sport_news_portal/web_application_features/most_popular_and_commentable/images/most_popular_commentable.png)

</details>

## Test Scenarios

1. Verify the Most Commentable content block
2. Verify the content of Most Commentable article
3. Verify clicking on Most Commentable article

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the Most Commentable content block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Observe the content of the Most Commentable block|This block is listed the 3 most commentable articles (most commentable based on page views for a specified time period) one below the other

### **#2. Verify the content of most commentable article**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Observe the content of the Most Commentable block|This block is listed the 3 most commentable articles (most commentable based on page views for a specified time period) one below the other
|4|Examine the content of each article|The Article includes:<br>- Thumbnail photo<br>- Headline (the right from the photo)<br>- Caption (under Headline)

### **#3. Verify clicking on Most Commentable article**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Observe the content of the Most Commentable block|This block is listed the 3 most commentable articles (most commentable based on page views for a specified time period) one below the other
|4|Click on any article|User is taken to the article page

</details>
