### Back to [View articles in the application](../../README.md) feature

# Allow users to view an article in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to view the article page
    So that I can read an article content

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the article content</i></b>

Given I am a user

When I view the article page
Then I see the following:
  - Article photo
  - Article headline, and metadata (including author and source)
  - Social network share buttons: Facebook, Twitter, Google +
  - Article content under the photo
  - The comments section under the article content
  - More articles section under the comment section
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the article page
2. Article full page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the article page:**

![Users see the article page](/sports_hub_portal/mobile_application_features/articles_view/images/application_article_page.png)

**2. Article full page:**

![Article full page](/sports_hub_portal/mobile_application_features/articles_view/images/article_page.png)

</details>

## Test cases

1. Verify the article content

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the article content**

|Preconditions|Steps|Expected result
------|-------|----------
||1) Go to any category</br>2) Select the article</br>3) Examine the article page content|2) The article page is opened</br>3) The article corresponds to the mockup|
</details>
