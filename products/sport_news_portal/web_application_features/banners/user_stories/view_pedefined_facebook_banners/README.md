### Back to [Banners on the portal](../../) feature

# Allow site users to view predefined Facebook banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view predefined Facebook banners on the portal

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views Facebook Video and Facebook Post banners in the sidebar section</i></b>

Given I am a site user

When I view any sport category page with the <b>Facebook Video</b> banner in the sidebar section
Then I see the most recent video added on the Sports Hub Facebook page
  And I see the following:
    - Heading <b>Facebook Video</b>
    - Video thumbnail
    - Video title
    - Like us on Facebook link and a like icon

When I click the video or the <b>Like us on Facebook</b> link
Then I am taken to the video on the Sports Hub Facebook page

When I click a like icon
Then I see the Facebook pop-up window where I can comment and like the video

When I view a page with the <b>Facebook Post</b> banner in the sidebar section
Then I see the most recent post added on the Sports Hub Facebook page
  And I see the following:
    - Heading <b>Facebook Post</b>
    - Post photo
    - Post headline
    - Like us on Facebook link and a like icon

When I click the photo or select the <b>Like us on Facebook</b> link
Then I am taken to the post on the Sports Hub Facebook page

When I click a <b>like</b> icon
Then I see the Facebook pop-up window where I can comment and like the post
</pre>

## Mockups

1. Users see <b>Facebook Video</b> and <b>Facebook Post</b> banners in the sidebar section

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Facebook Video and Facebook Post banners in the sidebar section:**

![Users see Facebook Video and Facebook Post banners in the sidebar section](/products/sport_news_portal/web_application_features/banners/images/banners_user_side.png)

</details>

## Test cases

1. Verify the content of the sports category page with the <b>Facebook Video</b> sidebar section
2. Verify selecting the <b>Facebook Video</b> section or the Like us on the Facebook link
3. Verify clicking the like button
4. Verify the content of the <b>Facebook Post</b> section on the right sidebar
5. Verify selecting the <b>Facebook Post</b> section or the Like us on the Facebook link
6. Verify clicking the like button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the sports category page with the Facebook Video sidebar section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Select any sports category page with the <b>Facebook Video</b> section|1) The <b>Facebook Video</b> section contains the most recent video and the following:</br>- Heading <b>Facebook Video</b></br>- Video thumbnail</br>- Video title</br>- Like us on Facebook link and a like icon|

### **#2. Verify selecting the Facebook Video section or the Like us on the Facebook link**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Select any sports category page with the <b>Facebook Video</b> section</br>2) Click the <b>Facebook Video</b> section|2) The user is redirected to the Facebook video page|

### **#3. Verify clicking the like button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Video</b> banner is enabled|1) Select any sports category page with the <b>Facebook Video</b> section</br>2) Click the <b>Like</b> button|2)  The Facebook pop-up window appears where I can comment and like the video|

### **#4. Verify the content of the Facebook Post section on the right sidebar**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Post</b> banner is enabled|1) Select any sports category page with the <b>Facebook Post</b> section|1) The <b>Facebook Post</b> section contains the most recent post and the following:</br>- Heading <b>Facebook Post</b></br>- Post photo</br>- Post headline</br>- Like us on Facebook link and a like icon|

### **#5. Verify selecting the Facebook Post section or the Like us on the Facebook link**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Post</b> banner is enabled|1) Select any sports category page with the <b>Facebook Post</b> section</br>2) Click the <b>Facebook Post</b> section|2) The user is redirected to the Facebook post page|

### **#6. Verify clicking the like button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Facebook Post</b> banner is enabled|1) Select any sports category page with the <b>Facebook Post</b> section</br>2) Click the <b>Like</b> button|2) The Facebook pop-up window appears where I can comment and like the post|

</details>
