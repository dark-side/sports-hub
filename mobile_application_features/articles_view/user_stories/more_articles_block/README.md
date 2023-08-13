### Back to [View articles in the application](../../README.md) feature

# Allow users to view More Articles block in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to see a section with more articles from the same category as the article I view

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the More Articles section</i></b>

Given I am a user

When I view the article page
Then I see a list of articles below the comments section including:
  - Heading <b>More Articles</b>
  - Article thumbnail photo
  - Article headline
  - Article summary/excerpt

When I tap an article photo, headline, or excerpt from <b>More</b> section
Then I am taken to that article page
  And I see the article page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>More Articles</b> block on the article page
2. Article full page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see More Articles block on the article page:**

![Users see More Articles block on the article page](/mobile_application_features/articles_view/images/application_more_articles.png)

**2. Article full page:**

![Article full page](/mobile_application_features/articles_view/images/article_page.png)

</details>

## Test cases

1. Verify tapping an article photo
2. Verify tapping an article headline
3. Verify tapping an article summary/excerpt

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify tapping an article photo**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the article page|1) Tap an article photo in the <b>More Articles</b> section|1) The user is redirected to that article page|

### **#2. Verify tapping an article headline**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the article page|1) Tap any article heading in the <b>More Articles</b> section|1) The user is redirected to that article page|

### **#3. Verify tapping an article summary/excerpt**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the article page|1) Tap an article summary/excerpt in the <b>More Articles</b> section|1) The user is redirected to that article page|
</details>
