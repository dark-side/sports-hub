### Back to [Articles User Side on the portal](../../) feature

# Allow users to share an article from the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to see block with articles that are from the same category as the article I view


## Acceptance criteria

    Scenario: A site user views a more articles block
    Given I am logged in as a site user

    When I view an article page
    Then I see a list of articles below the comments section including:
	  1. Heading “More Articles”
      2. Article thumbnail photo
      3. Article Headline
      4. Article Summary/Excerpt
    When I click on an article photo, headline, or excerpt
	Then I am taken to that article’s page
      And I see the number of articles shown is configurable in the CMS
      And I see the articles selected are from the same category as the article I am view

## Mockups

1. User sees Article page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Article page:**

![Article Screen](/products/sport_news_portal/web_application_features/articles_user_side/images/article_page.png)


</details>

## Test Scenarios

1. Verify a list of articles below the comments section
2. Verify clicking on an article photo
3. Verify clicking on an article headline
4. Verify clicking on article Summary/Excerpt

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify a list of articles below the comments section**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe a list of articles below the comments section|The list of articles below the comments section including:<br> - Heading "More Articles"<br> - Article thumbnail photo<br> - Article Headline<br> - Article Summary/Excerpt

### **#2. Verify clicking on an article photo**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe a list of articles below the comments section|The list of articles below the comments section including:<br> - Heading "More Articles"<br> - Article thumbnail photo<br> - Article Headline<br> - Article Summary/Excerpt
|4|Click on Article thumbnail photo|User is taken to that article’s page

### **#3. Verify clicking on an article headline**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe a list of articles below the comments section|The list of articles below the comments section including:<br> - Heading "More Articles"<br> - Article thumbnail photo<br> - Article Headline<br> - Article Summary/Excerpt
|4|Click on Article Headline|User is taken to that article’s page

### **#4. Verify clicking on article Summary/Excerpt**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe a list of articles below the comments section|The list of articles below the comments section including:<br> - Heading "More Articles"<br> - Article thumbnail photo<br> - Article Headline<br> - Article Summary/Excerpt
|4|Click on Article Summary/Excerpt|User is taken to that article’s page

</details>

