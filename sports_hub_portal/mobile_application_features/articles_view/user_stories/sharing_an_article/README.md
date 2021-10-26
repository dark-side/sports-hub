### Back to [View articles in the application](../../) feature

# Allow users to share an article from the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to share the article on my social networks accounts and my messengers

## Acceptance criteria

<pre>
<b><i>Scenario: A user shares the article on the selected service</i></b>

Given I am a user

When I view the article page
Then I see a share icon

When I tap the share icon
Then I see a window where I can select the service to share the article

When I select the service
Then I see that the article is shared
</pre>

## Mockups

1. Users see an icon to share the article
2. Article full page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see an icon to share the article:**

![Users see an icon to share the article](/sports_hub_portal/mobile_application_features/articles_view/images/application_article_page.png)

**2. Article full page:**

![Article full page](/sports_hub_portal/mobile_application_features/articles_view/images/article_page.png)

</details>

## Test cases

1. Verify redirection to the appropriate page while tapping a share button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify redirection to the appropriate page while tapping a share button**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Tap any article</br>2) Tap a share icon|2) The user is prompted to select the service|
</details>
