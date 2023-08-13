### Back to [Sports videos on the portal](../../README.md) feature

# Allow site users to share videos on social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to share sports videos on my social network account

## Acceptance criteria

<pre>
<b><i>Scenario: A site user shares sports videos</i></b>

Given I am a site user

When I view a specific video page, video sharing is enabled and at least one social network is configured for sharing
Then I see the <b>Share</b> button on the video in the upper right corner

When I hover over the <b>Share</b> button
Then I see social networks icons

When I click any of social networks icon
Then I see the video is shared on my social network account
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. User hovers over the <b>Share</b> button and sees social networks icons

<details>
  <summary>Click here to see mockups details</summary>

**1. User hovers over the Share button and sees social networks icons:**

![User hovers over the Share button and sees social networks icons](/web_application_features/video_page/images/user_video_share.png)

</details>

## Test cases

1. Verify sharing the video on social network

<details>
  <summary>Click here to see test cases details</summary>

### **#4. Verify sharing the video on social network**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page on the Sports Hub site|1) Hover over the <b>Share</b> button</br>2) Click some social network|2) The pop-up window opens allowing the user to share the current video on the social network|

</details>
