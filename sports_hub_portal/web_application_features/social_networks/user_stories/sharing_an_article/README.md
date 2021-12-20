### Back to [Social networks on the portal](../../) feature

# Allow users to share an article from the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to click the social network share buttons
    So that I can share an article on my social network account

## Acceptance criteria

<pre>
<b><i>Scenario: A site user shares the article on the selected service</i></b>

Given I am a site user

When at least one social network is configured for sharing
Then I see the <b>Share</b> button on the article page

When I view the article page and hover over the <b>Share</b> button
Then I see social network icons that are configured for sharing

When I click <b>Facebook</b>, <b>Twitter</b>, or <b>Google+</b> icon
Then I see a prompt to authentication and permissions request page
  And I can comment and share an article on the selected service
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see share button on the article page
2. Users see social network icons when hovering the <b>Share</b> button

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see share button on the article page:**

![Users see share button on the article page](/sports_hub_portal/web_application_features/social_networks/images/article_page.png)

**2. Users see social network icons when hovering the Share button:**

![Users see social network icons when hovering the Share button](/sports_hub_portal/web_application_features/social_networks/images/article_share_icon_hover.png)

</details>

## Test cases

1. Verify that authentication prompt appears on clicking a social network share button
2. Verify the ability to comment on the article and share it in the selected social network

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that authentication prompt appears on clicking a social network share button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the Sports Hub site</br>- On the **Home** page|1) Select any article</br>2) Сlick to share the article with **Facebook**, **Twitter**, or **Google+**|2) The user is prompted to authentication and permissions request page|

### **#2. Verify the ability to comment on the article and share it in the selected social network**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- On the Sports Hub site</br>- On the **Home** page|1) Select any article</br>2) Сlick to share the article with **Facebook**, **Twitter**, or **Google+**</br>3) Enter information in the authentication window</br>4) Write a comment on the article or share it in the selected social network| 4) Users can comment and share articles in the selected social network|
</details>
