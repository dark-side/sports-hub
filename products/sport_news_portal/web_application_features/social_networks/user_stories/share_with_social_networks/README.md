### Back to [Social networks on the portal](../../) feature

# Allow users to share Sport News portal on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to click on the Share social networks icons
    So that I can share the Sport News portal

## Acceptance criteria

<pre>
<b><i>Scenario: A site user shares portal by clicking on configured social networks icons</i></b>

Given I am a site user

When I view any page on the site
Then I see the Share label and the following social network icons that are configured in the site header (Facebook, Twitter, Google+)

When I click any of these icons
Then I see a confirmation to share window of the social network is open
  And the portal is shared
</pre>

## Mockups

1. User sees Share icons in the site header
2. User sees sharing in Facebook example

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Share icons in the site header:**

![User sees Share icons in the site header](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

**2. User sees sharing in Facebook example:**

![User sees sharing in Facebook example](/products/sport_news_portal/web_application_features/social_networks/images/sharing_in_facebook_example.png)

</details>

## Test cases

1. Verify social network icons
2. Verify sharing the portal on Facebook
3. Verify sharing the portal on Twitter
4. Verify ability to share the portal in Google+

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify social network icons**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine the social network icons|2) User sees the configured social network icons in the site header (Facebook, Twitter, Google+)|

### **#2. Verify sharing the portal on Facebook**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine the social network icons</br>3) Click Facebook|3) The popup window is opened allowing a user to share the portal on Facebook|

### **#3. Verify sharing the portal on Twitter**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine the social network icons</br>3) Click Twitter|3) The popup window is opened with the ability to share the portal on Twitter|

### **#4. Verify ability to share the portal in Google+**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine the social network icons</br>3) Click Google+|3) The popup window is opened allowing a user to share the portal on Google+|

</details>
