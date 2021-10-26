### Back to [Banners in the application](../../) feature

# Allow users to view configured banners in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to view banners after the main page content
    So that I can see reminders about upcoming sport events, important updates, etc.

## Acceptance criteria

<pre>
<b><i>Scenario: A user views banners after the main page content</i></b>

Given I am a user

When I view a page within the category that has some banner(s) published
Then I see the banner(s) photo in the banner section

When there are more than one banner configured for the category
Then I see banners are rotating every 3 seconds
</pre>

## Mockups

1. Users see a banner at the bottom of the page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a banner at the bottom of the page:**

![Users see a banner at the bottom of the page](/products/sports_hub_portal/mobile_application_features/banners/images/application_banner_user_side.png)

</details>

## Test cases

1. Verify that users can view the published banners
2. Verify that banners are rotating

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users can view the published banners**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Banners are published for a category|1) Go to the category</br>2) Examine the banner section after the main page content|2) There are banners with photo in the appropriate section|

### **#2. Verify that banners are rotating**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Banners are published for a category</br>- There are more than one banner in the category|1) Go to the category</br>2) Wait for 3 seconds</br>3) Examine the banner section</br>4) Wait till all banners from the category are shown|3) Banner is changed in the section</br>4) First banner is shown again|

</details>
