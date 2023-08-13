### Back to [Social networks on the application](../../README.md) feature

# Allow users to follow Sports Hub on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to follow the Sports Hub on social networks

## Acceptance criteria

<pre>
<b><i>Scenario: A user follows the Sports Hub using one of the configured social networks (Facebook, Twitter, Google +, YouTube)</i></b>

Given I am a user

When I view any page
Then I see the <b>Follow us</b> icons for the configured by admin social networks in the footer (Facebook, Twitter, Google+, YouTube) in the footer

When I tap any of these icons
Then I go to the Sports Hub page on that social network
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Follow us</b> icons in the footer

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Follow us icons in the footer:**

![Users see Follow us icons in the footer](/mobile_application_features/social_networks/images/application_follow_us_icons.png)

</details>

## Test cases

1. Verify social networks icons in the main menu
2. Verify tapping the Facebook icon
3. Verify tapping the Twitter icon
4. Verify tapping the Google+ icon
5. Verify tapping the YouTube icon

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify social networks icons in the main menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Examine icons in the main menu|1) The following icons are present:</br>- Facebook</br>- Twitter</br>- Google+</br>- YouTube|

### **#2. Verify tapping the Facebook icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Tap the main menu icon</br>2) Tap the Facebook icon|2) The user goes to the Sports Hub page on Facebook|


### **#3. Verify tapping the Twitter icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Tap the main menu icon</br>2) Tap the Twitter icon|2) The user goes to the Sports Hub page on Twitter|

### **#4. Verify tapping the Google+ icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Tap the main menu icon</br>2) Tap the Google+ icon|2) The user goes to the Sports Hub page on Google+|

### **#5. Verify tapping the YouTube icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Tap the main menu icon</br>2) Tap the YouTube icon|2) The user goes to the Sports Hub page on YouTube|

</details>
