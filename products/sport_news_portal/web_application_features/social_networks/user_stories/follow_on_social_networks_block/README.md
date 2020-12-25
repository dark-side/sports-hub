### Back to [Social Networks on the portal](../../) feature

# Allow users to follow the portal on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to follow the Sport News portal on the social networks

## Acceptance criteria

<pre>
Scenario: A site user follows the Sport News portal using one of the configured social networks (Facebook, Twitter, Google +, Youtube)
Given I am a site user

When I view any page of the Sport News site
Then I see the Follow icons for Facebook, Twitter, Google+, and YouTube on the left sidebar menu

When I click any of these icons
Then I go to the Sport News page on that site
</pre>

## Mockups

1. User sees Follow icons in the navigation menu

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Follow icons in the site header:**

![User sees Follow icons in the navigation menu](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test cases

1. Verify social network icons at the Navigation menu
2. Verify clicking on the Facebook icon
3. Verify clicking on the Twitter icon
4. Verify clicking on the Google+ icon
5. Verify clicking on the YouTube icon

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify social network icons at the Navigation menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine icons on the left sidebar menu|2) The following icons are present: Facebook, Twitter, Google+, YouTube|

### **#2. Verify clicking on the Facebook icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine icons on the left sidebar menu</br>3) Click on the Facebook icon|2) The following icons are present: Facebook, Twitter, Google+, YouTube</br>3) User goes to the Sport News page on Facebook|

### **#3. Verify clicking on the Twitter icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine icons on the left sidebar menu</br>3) Click on the Twitter icon|2) The following icons should be present: Facebook, Twitter, Google+, YouTube</br>3) User goes to the Sport News page on Twitter|

### **#4. Verify clicking on the Google+ icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine icons on the left sidebar menu</br>3) Click on the Google+ icon|2) The following icons are present: Facebook, Twitter, Google+, YouTube</br>3) User goes to the Sport News page on Google+|

### **#5. Verify clicking on the YouTube icon**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go to the Sport News site</br>2) Examine icons on the left sidebar menu</br>3) Click on the YouTube icon|2) The following icons should be present: Facebook, Twitter, Google+, YouTube</br>3) User goes to the Sport News page on YouTube|

</details>
