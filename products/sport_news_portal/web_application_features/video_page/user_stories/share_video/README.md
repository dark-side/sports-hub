### Back to [Sports videos on the portal](../../) feature

# Allow site users to share videos on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to share sports videos on my social network account

## Acceptance criteria

<pre>
<b><i>Scenario: A site user shares sports videos</i></b>

Given I am a site user

When I view a spesific video page and video sharing is enabled
Then I see <b>Share</b> button on the video in the upper right corner

When I hover over the <b>Share</b> button
Then I see social networks icons

When I click any of social networks icon
Then I see the video being shared on my social network account
</pre>

## Mockups

1. User hovers over the Share button and sees social networks icons

<details>
  <summary>Click here to see mockups details</summary>

**1. User hovers over the Share button and sees social networks icons:**

![User hovers over the Share button and sees social networks icons](/products/sport_news_portal/web_application_features/video_page/images/user_video_share.png)

</details>

## Test cases

1. Verify sharing the video on social network

<details>
  <summary>Click here to see test cases details</summary>

### **#4. Verify sharing the video on social network**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page of the Sport News site|1) Hover over the <b>Share</b> button</br>2) Click some social network|2) The popup window is opened allowing a user to share the current video on the social network|

</details>
