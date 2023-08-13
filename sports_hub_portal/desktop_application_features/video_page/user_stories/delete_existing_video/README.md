### Back to [Sports videos on the portal](../../README.md) feature

# Allow admin users to delete existing videos

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete existing videos

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes the existing video</i></b>

Given I am logged in as an admin user

When I select the <b>Video</b> link on the admin side 
Then I see the list of blocks with videos

When I hover over any video
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for a video
Then I see <b>Delete</b> menu item is present

When I select <b>Delete</b> menu item
Then I see confirmation dialog

When I click <b>Cancel</b>
Then I see the dialog disappears and video is still present

When I click <b>Delete</b>
Then I see the "The video is successfully deleted" flash message
  And the video is removed from the list
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions for the published video
2. Admin user sees a delete confirmation dialog

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the published video:**

![Admin user sees actions for the published video](/sports_hub_portal/desktop_application_features/video_page/images/video_actions.png)

**2. Admin user sees a delete confirmation dialog:**

![Admin user sees a delete confirmation dialog](/sports_hub_portal/desktop_application_features/video_page/images/delete_confirmation_from_index.png)

</details>

## Test cases

1. Verify that admin is able to delete an unpublished video
2. Verify that admin is able to delete a published video
3. Verify that admin is able to cancel deleting of any video

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to delete an unpublished video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) On the confirmation popover, click the <b>Delete</b> button|3) "The video is successfully deleted" flash message appears and video is deleted from the list|

### **#2. Verify that admin is able to delete a published video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is a published video|1) Hover over a published video</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) On the confirmation popover, click the <b>Delete</b> button|3) "The video is successfully deleted" flash message appears and video is deleted from the list|

### **#3. Verify that admin is able to cancel deleting of any video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Hover over any video</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) On the confirmation popover, click the <b>Cancel</b> button|3) The video is present in the list|

</details>
