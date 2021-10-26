### Back to [Banners in the application](../../) feature

# Allow users to view predefined Facebook banners in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view predefined Facebook Video and Post banners after the main page content
    So that I can quickly view the most recent sports video or post added on Facebook

## Acceptance criteria

<pre>
<b><i>Scenario: A user views Facebook Video and Facebook Post banners</i></b>

Given I am a user

When I view any sport category page with the Facebook Video banner section
Then I see the following:
  - Heading <b>Facebook Video</b>
  - Video thumbnail
  - Video title
  - <b>Like us on Facebook</b> link
  - Facebook like button
  - Current number of Facebook likes

When I tap the video or select Like us on Facebook link
Then I am taken to the video on the Sports Hub Facebook page

When I tap <b>Like us on Facebook</b>
Then I see the Facebook pop-up window where I can comment and like the video

When I tap the video section
Then I am taken to the video page
  And I see the most recent video added on the Sport News Facebook page

When I view a page with the Facebook Post banner section after the main page content
Then I see the following:
  - Heading <b>Facebook Video</b>
  - Post photo
  - Post headline
  - <b>Like us on Facebook</b> link
  - The Facebook like button
  - Current number of Facebook likes

When I tap the photo or select the Like us on Facebook link
Then I am taken to the post on the Sports Hub Facebook page

When I tap <b>Like us on Facebook</b>
Then I see the Facebook pop-up window where I can comment and like the story
</pre>

## Mockups

1. Users see <b>Facebook Video</b> banner at the bottom of the page
2. Users see <b>Facebook Post</b> banner at the bottom of the page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Facebook Video banner at the bottom of the page:**

![Users see Facebook Video banner at the bottom of the page](/sports_hub_portal/mobile_application_features/banners/images/application_facebook_video_banner.png)

**2. Users see Facebook Post banner at the bottom of the page:**

![Users see Facebook Post banner at the bottom of the page](/sports_hub_portal/mobile_application_features/banners/images/application_facebook_post_banner.png)

</details>

## Test cases

1. Verify the content of sport category page with the <b>Facebook Video</b> banner section
2. Verify tapping the <b>Facebook Video</b> section or the <b>Like us on Facebook</b> link
3. Verify tapping the like button on <b>Facebook Video</b>
4. Verify that the <b>Facebook Video</b> section includes the most recent video related to the section of the application
5. Verify the content of the <b>Facebook Post</b> banner section
6. Verify tapping the photo or the <b>Like us on Facebook</b> link
7. Verify tapping the Like button on <b>Facebook Post</b>

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of sport category page with the Facebook Video banner section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Select on any sports category page with the <b>Facebook Video</b> banner section|1) On the opened page there is the following:</br>- Heading <b>Facebook Video</b></br>- Video thumbnail</br>- Video title</br>- Like us on Facebook link</br>- The Facebook like button</br>- Current number of Facebook likes|

### **#2. Verify tapping the Facebook Video section or the Like us on Facebook link**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Select any sports category page with <b>Facebook Video</b> banner section</br>2) Tap <b>Facebook Video</b> section|2) The user is redirected to the video article page|

### **#3. Verify tapping the like button on Facebook Video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Examine the <b>Facebook Video</b> banner section</br>2) Tap the <b>Like</b> icon|2) The Facebook pop-up window appears where I can comment and like the video|

### **#4. Verify that the Facebook Video section includes the most recent video related to the section of the application**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Tap the MLB (baseball) section of the sports category page</br>2) Observe the <b>Facebook Video</b> banner section|2) The <b>Facebook Video</b> banner section contains the most recent video related to baseball|

### **#5. Verify the content of the Facebook Post banner section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Post</b> banner is enabled|1) Examine the banner section after the main page content|1) There is a block with the following information pulled from the Sports Hub Facebook page:</br>- Heading <b>Facebook Post</b></br>- Post photo</br>- Post headline</br>- The <b>Like us on Facebook</b> link</br>- The Facebook like button</br>- Current number of Facebook likes|

### **#6. Verify tapping the photo or the Like us on Facebook link**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Post</b> banner is enabled|1) Examine the <b>Facebook Post</b> banner section</br>2) Select the <b>Like us on Facebook</b> link|2) The user is taken to the featured story on the Sports Hub Facebook page|

### **#7. Verify tapping the Like button on Facebook Post**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Post</b> banner is enabled|1) Examine the <b>Facebook Post</b> banner section</br>2) Tap the <b>Like</b> icon|2) The Facebook pop-up window appears where I can comment and like the story|

</details>
