### Back to [Articles User Side on the portal](../../) feature

# Allow users to view an article on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to view an article page
    So that I can read an article content

## Acceptance criteria

<pre>
Scenario: A site user views an article content
Given I am a site user

When I view an article page
Then I see the following:
  1. Article photo
  2. Photo, article headline, and metadata (including author and source) in the upper-right corner of the photo (see mockup)
  3. Social network share buttons: Facebook, Twitter, Google +, next to the Share button in the headline above the article photo
  4. Article content under the photo
  5. The comments section under the article content
  6. More articles section under the comment section
</pre>

## Mockups

1. User sees an article page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees an article page:**

![User sees an article page](/products/sport_news_portal/web_application_features/articles_user_side/images/article_page.png)

</details>

## Test cases

1. Verify an article content

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify an article content**

|Preconditions|Steps|Expected result
------|-------|----------
||1) Go to any category</br>2) Click on the article</br>3) Examine an article page content|2) The article page is opened</br>3) The article corresponds to the mockup|
</details>
