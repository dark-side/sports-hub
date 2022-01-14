### Back to [Sports videos](../../) feature

# Allow users to share video from the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to share video on my social networks accounts and my messengers

## Acceptance criteria

<pre>
<b><i>Scenario: A user shares video on the selected service</i></b>

Given I am a user

When I view the video page
Then I see a share icon

When I tap the share icon
Then I see a window where I can select the service to share the article

When I select the service
Then I see that the article is shared
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Share</b> icon on video page
2. Full video view page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Share icon on video page:**

![Users see Share icon on video page](/sports_hub_portal/mobile_application_features/video_page/images/application_video_view_page.png)

**2. Full video view page:**

![Full video view page](/sports_hub_portal/mobile_application_features/video_page/images/video_view_page.png)

</details>

## Test cases

1. Verify sharing the video on social network

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify sharing the video on social network**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Video</b> page|1) Tap share icon|1) The user is promted to share the current video on services|

</details>
