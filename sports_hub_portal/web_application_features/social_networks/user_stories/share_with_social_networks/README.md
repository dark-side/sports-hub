### Back to [Social networks on the portal](../../README.md) feature

# Allow users to share Sports Hub portal on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to click the Share social networks icons
    So that I can share the Sports Hub portal

## Acceptance criteria

<pre>
<b><i>Scenario: A site user shares portal by clicking configured social networks icons</i></b>

Given I am a site user

When I view any page on the site
Then I see the <b>Share</b> label and the following social network icons that are configured in the site header (Facebook, Twitter, Google+)

When I click any of these icons
Then I see a confirmation to share window of the social network opens
  And the portal is shared
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Share</b> icons in the site header
2. Users see sharing in Facebook example

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Share icons in the site header:**

![Users see Share icons in the site header](/sports_hub_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

**2. Users see sharing in Facebook example:**

![Users see sharing in Facebook example](/sports_hub_portal/web_application_features/social_networks/images/sharing_in_facebook_example.png)

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
||1) Go to the Sports Hub site</br>2) Examine the social network icons|2) Users see the configured social network icons in the site header (Facebook, Twitter, Google+)|

### **#2. Verify sharing the portal on Facebook**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine the social network icons</br>3) Click <b>Facebook</b>|3) The pop-up window opens allowing users to share the portal on Facebook|

### **#3. Verify sharing the portal on Twitter**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine the social network icons</br>3) Click <b>Twitter</b>|3) The pop-up window opens allowing users to share the portal on Twitter|

### **#4. Verify ability to share the portal in Google+**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine the social network icons</br>3) Click <b>Google+</b>|3) The pop-up window opens allowing users to share the portal on Google+|

</details>
