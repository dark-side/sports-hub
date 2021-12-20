### Back to [Articles - user side on the portal](../../) feature

# Allow users to view an article on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to view an article page
    So that I can read an article content

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the article content</i></b>

Given I am a site user

When I view the article page
Then I see the following:
  1. Article photo
  2. Photo, article headline, and metadata (including author and source) in the upper-right corner of the photo (see mockup)
  3. Article content under the photo
  4. More articles section under the comment section
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the article page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the article page:**

![Users see the article page](/sports_hub_portal/web_application_features/articles_user_side/images/article_page.png)

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
