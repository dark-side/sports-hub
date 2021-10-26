### Back to [Articles - user side on the portal](../../) feature

# Allow users to view More Articles block on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to see a section with more articles from the same category as the article I view

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the More Articles section</i></b>

Given I am a site user

When I view the article page
I see a list of articles below the comments section including:
- Heading <b>More Articles</b>
- Article thumbnail photo
- Article headline
- Article summary/excerpt

When I click an article photo, headline, or excerpt from <b>More Articles</b> section
Then I am taken to that article page
  And I see the article page

</pre>

## Mockups

1. Users see <b>More Articles</b> block on the article page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see More Articles block on the article page:**

![Users see More Articles block on the article page](/sports_hub_portal/web_application_features/articles_user_side/images/article_page.png)

</details>

## Test cases

1. Verify clicking an article photo
2. Verify clicking an article headline
3. Verify clicking an article summary/excerpt

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify clicking an article photo**

|Preconditions|Steps|Expected result
--------------|-----|----------
|The user is on the article page|1) Click an article photo in the <b>More Articles</b> section|1) The user is redirected to that article page|

### **#2. Verify clicking an article headline**

|Preconditions|Steps|Expected result
--------------|-----|----------
|The user is on the article page|1) Click any article heading|1) The user is redirected to that article page|

### **#3. Verify clicking an article summary/excerpt**

|Preconditions|Steps|Expected result
--------------|-----|----------
|The user is on the article page|1) Click an article summary/excerpt|1) The user is redirected to that article page|

</details>
