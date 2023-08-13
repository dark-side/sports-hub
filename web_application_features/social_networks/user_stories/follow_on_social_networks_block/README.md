### Back to [Social networks on the portal](../../README.md) feature

# Allow users to follow the portal on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to follow the Sports Hub portal on social networks

## Acceptance criteria

<pre>
<b><i>Scenario: A site user follows the Sports Hub portal using one of the configured social networks (Facebook, Twitter, Google +, YouTube)</i></b>

Given I am a site user

When I view any page of the Sports Hub site
Then I see the Follow icons for Facebook, Twitter, Google+, and YouTube on the left sidebar menu

When I click any of these icons
Then I go to the Sports Hub page on that site
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Follow</b> icons in the navigation menu

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Follow icons in the site header:**

![Users see Follow icons in the navigation menu](/web_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test cases

1. Verify social network icons on the navigation menu
2. Verify clicking the Facebook icon
3. Verify clicking the Twitter icon
4. Verify clicking the Google+ icon
5. Verify clicking the YouTube icon

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify social network icons on the navigation menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine icons on the left sidebar menu|2) The following icons are present: Facebook, Twitter, Google+, YouTube|

### **#2. Verify clicking the Facebook icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine icons on the left sidebar menu</br>3) Click the Facebook icon|2) The following icons are present: Facebook, Twitter, Google+, YouTube</br>3) The user goes to the Sports Hub page on Facebook|

### **#3. Verify clicking the Twitter icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine icons on the left sidebar menu</br>3) Click the Twitter icon|2) The following icons should be present: Facebook, Twitter, Google+, YouTube</br>3) The user goes to the Sports Hub page on Twitter|

### **#4. Verify clicking the Google+ icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine icons on the left sidebar menu</br>3) Click the Google+ icon|2) The following icons are present: Facebook, Twitter, Google+, YouTube</br>3) The user goes to the Sports Hub page on Google+|

### **#5. Verify clicking the YouTube icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sports Hub site</br>2) Examine icons on the left sidebar menu</br>3) Click the YouTube icon|2) The following icons should be present: Facebook, Twitter, Google+, YouTube</br>3) The user goes to the Sports Hub page on YouTube|

</details>
