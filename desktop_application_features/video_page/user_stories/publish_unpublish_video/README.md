### Back to [Sports videos on the portal](../../README.md) feature

# Allow admin users to publish/unpublish existing videos

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to publish/unpublish existing videos

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user publish/unpublish an existing video</i></b>

Given I am logged in as an admin user

When I select the <b>Video</b> link on the admin side
Then I see the list of blocks with videos

When I hover over any video
Then I see the ellipsis (...) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an unpublished video
Then I see <b>Publish</b> menu item is present

When I click <b>Publish</b> menu item
Then I see "The video is successfully published" flash message
  And the status of the video changed to <b>Published</b>
  And the video is visible for users

When I click "<b>...</b>" the menu icon for a published video
Then I see the <b>Unpublish</b> menu item present

When I click the <b>Unpublish</b> menu item
Then I see "The video is successfully unpublished" flash message
  And the status of video changed to <b>Unpublished</b>
  And the video is not visible for users anymore
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions for the published video

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the published video:**

![Admin user sees actions for the published video](/desktop_application_features/video_page/images/video_actions.png)

</details>

## Test cases

1. Verify that admin is able to publish an existing unpublished video
2. Verify that admin is able to unpublish an existing published video

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to publish an existing unpublished video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Publish</b> menu item|2) "The video is successfully published" flash message appears and users can see the video|

### **#2. Verify that admin is able to unpublish an existing published video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is a published video|1) Hover over a published video</br>2) Click "<b>...</b>" button > <b>Unpublish</b> menu item|2) "The video is successfully unpublished" flash message appears and users can not see the video|

</details>
