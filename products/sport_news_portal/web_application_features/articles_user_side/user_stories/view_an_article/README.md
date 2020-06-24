### Back to [Articles User Side on the portal](/../../) feature

# Allow users to view an article on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to view an article page 
    So that I can read an article content


## Acceptance criteria

    Scenario: A site user views an article content
    Given I am logged in as a site user

    When I view an article page
    Then I see the following:
      1. Article photo (or video if it is a video article)
      2. Photo credit, article headline and article metadata (including author and source) in the square on the right side of the foto (see mockup)
      3. Social Sharing buttons (Email, Facebook, Twitter) next to "Share" text in the top right corner above the article photo or video
      4. Article Content under the photo or video
      5. More Articles Block at the page bottom

## Mockups

1. User sees Article page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Article page:**

![Article Screen](/products/sport_news_portal/web_application_features/articles_user_side/images/article_page.png)


</details>

## Test Scenarios

1. Verify an article content

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify an article content**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe an article content|Article content includes:<br> - Article photo (or video if it is a video article)<br> - Photo credit, article headline and article metadata (including author and source) in the square on the right side of the foto<br> - Social Sharing buttons (Email, Facebook, Twitter) next to "Share" text in the top right corner above the article photo or video<br> - Article Content under the photo or video<br> - Comments Section under the article content<br> - More Articles Block under the comment section

</details>
