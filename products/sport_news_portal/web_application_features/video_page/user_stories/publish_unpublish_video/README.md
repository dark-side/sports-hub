### Back to [Sports videos on the portal](../../) feature

# Allow admin users to publish/unpublish an existing video

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to publish/unpublish an existing video

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user publish/unpublish an existing video</i></b>

Given I am logged in as an admin user

When I click the <b>Videos</b> link on the admin side
Then I see the list of blocks with videos

When I hover over any video
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." the menu icon for an unpublished video
Then I see the <b>Publish</b> menu item present

When I click <b>Publish</b> menu item
Then I see "The video is successfully published" flash message
  And the status of the video changed to <b>Published</b>
  And the video is visible for users

When I click "..." the menu icon for a published video
Then I see the <b>Unpublish</b> menu item present

When I click the <b>Unpublish</b> menu item
Then I see "The video is successfully unpublished" flash message
  And the status of video changed to <b>Unpublished</b>
  And the video is not visible for users anymore
</pre>

## Mockups

1. Admin user sees actions for the published video

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the published video:**

![Admin user sees actions for the published video](/products/sport_news_portal/web_application_features/video_page/images/video_actions.png)

</details>

## Test cases

1. Verify that admin is able to publish an existing unpublished video
2. Verify that admin is able to Unpublish an existing published

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to publish an existing unpublished video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Publish</b> menu item|2) "The video is successfully published" flash message appears and the users can see the video|

### **#2. Verify that admin is able to Unpublish an existing published**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is a published video|1) Hover over a published video</br>2) Click "..." button -> <b>Unpublish</b> menu item|2) "The video is successfully unpublished" flash message appears and the users can not see the video|

</details>
