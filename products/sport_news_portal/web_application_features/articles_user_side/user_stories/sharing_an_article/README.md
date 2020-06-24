### Back to [Articles User Side on the portal](../../) feature

# Allow users to share an article from the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to click on social network icon 
    So that I can share an article with my social network account


## Acceptance criteria

    Scenario: A site user shares the article on the selected service
    Given I am logged in as a site user

    When I view an article page and click a social sharing icon
    Then I see a prompt to authentication and permissions request page
      And I am able comment and share the article on the selected service

## Mockups

1. User sees Article page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Article page:**

![Article Screen](/products/sport_news_portal/web_application_features/articles_user_side/images/article_page.png)


</details>

## Test Scenarios

1. Verify authentication prompt clicking on a social sharing icon
2. Verify ability to comment and share the article on the selected service

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify authentication prompt clicking on a social sharing icon**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in the user account|
|3|Сlick on a social sharing icon|User is prompted to authentication and permissions request page

### **#2. Verify ability to comment and share the article on the selected service**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to user account|
|3|Сlick on a social sharing icon|
|4|Fill in an authentication prompt|
|5|Try to comment or share the article on the selected service|User is able to comment and share the article on the selected service

</details>

