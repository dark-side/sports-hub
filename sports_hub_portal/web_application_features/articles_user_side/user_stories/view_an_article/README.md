### Back to [Articles - user side on the portal](../../) feature

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
<b><i>Scenario: A site user views the article content</i></b>

Given I am a site user

When I view the article page
Then I see the following:
  1. Article photo
  2. Photo, article headline, and metadata (including author and source) in the upper-right corner of the photo (see mockup)
  3. Social network share buttons: <b>Facebook</b>, <b>Twitter</b>, <b>Google +</b>, next to the <b>Share</b> button in the headline above the article photo
  4. Article content under the photo
  5. The comments section under the article content
  6. More articles section under the comment section
</pre>

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
