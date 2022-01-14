### Back to [Sports videos on the portal](../../) feature

# Allow admin users to edit existing videos

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to edit existing unpublished videos

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits the existing unpublished video</i></b>

Given I am logged in as an admin user

When I select the <b>Video</b> link on the admin side
Then I see the list of blocks with videos

When I hover over an unpublished video
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." the menu icon for unpublished video
Then I see the <b>Edit</b> menu item is present

When I select <b>Edit</b> menu item
Then I see a pre-populated form with video details:
  - Play and pause the video, enter a full-screen video mode, configure video volume and video settings
  - <b>Video</b> title field
  - The <b>Preview</b> icon in the upper-right corner of the page
  - The <b>Comments Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> buttons in the upper-right corner of the page (<b>Save</b> disabled until any changes are made)

When I select the <b>Preview</b> link button
Then I see how this video is shown for users

When I make any changes in the form
Then I see the <b>Save</b> button is enabled

When I click the <b>Save</b> button
Then I see the page with a list of the videos
  And I see that my updated video appears at the top of the list in <b>Unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I click <b>Confirm</b>
Then I see the page with a list of the videos
  And changes to the video are not saved
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user clicks to upload new video on the edit page and sees a pop-up window
2. Admin user sees a video form
3. Admin user hovers over the uploaded video
4. Admin user sees a success save flash message
5. Admin user sees a delete confirmation dialog
6. Admin user sees a cancel confirmation dialog
7. Admin user sees a video preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user clicks to upload new video on the edit page and sees a pop-up window:**

![Admin user clicks to upload new video on the edit page and sees a pop-up window](/sports_hub_portal/desktop_application_features/video_page/images/new_video_edit_popup.png)

**2. Admin user sees a new video form:**

![Admin user sees a new video form](/sports_hub_portal/desktop_application_features/video_page/images/video_form.png)

**3. Admin user hovers over the uploaded video:**

![Admin user hovers over the uploaded video](/sports_hub_portal/desktop_application_features/video_page/images/hover_over_video.png)

**4. Admin user sees a success save flash message:**

![Admin user sees a success save flash message](/sports_hub_portal/desktop_application_features/video_page/images/success_save_message.png)

**5. Admin user sees a delete confirmation dialog:**

![Admin user sees a delete confirmation dialog](/sports_hub_portal/desktop_application_features/video_page/images/delete_confirmation.png)

**6. Admin user sees a cancel confirmation dialog:**

![Admin user sees a cancel confirmation dialog](/sports_hub_portal/desktop_application_features/video_page/images/cancel_confirmation.png)

**7. Admin user sees a video preview page:**

![Admin user sees a video preview page](/sports_hub_portal/desktop_application_features/video_page/images/video_preview.png)

</details>

## Test cases

1. Verify that admin is able to change a video to the edited video
2. Verify that admin is not able to save empty required fields to the edited video
3. Verify that admin is able to preview the edited video
4. Verify that admin is able to save the edited video with all valid data updated
5. Verify that the <b>Comments</b> section can be hidden for the edited video
6. Verify that the <b>Comments</b> section can be shown for the edited video

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to change a video to the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) In the video section, click <b>Add new video</b></br>4) Enter a video link and click <b>Add</b></br>5) Click <b>Save</b>|5) Admin user is redirected to the list of videos. The video is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to save empty required fields to the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) In the <b>Video title</b> required field, delete data</br>4) Click <b>Save</b></br>5) Fill in the <b>Video title</b> required field</br>6) Hover over the video</br>7) Click the <b>Delete</b> icon</br>8) Click <b>Save</b>|4) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>8) The required fields are highlighted in red. The validation message "Fill in all required fields" appears|

### **#3. Verify that admin is able to preview the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Make some changes</br>4) Select the <b>Preview</b> link</br>5) Select <b>Back to edit page</b> link|4) The video is shown as it will appear for users</br>5) The video is back to edit mode|

### **#4. Verify that admin is able to save the edited video with all valid data updated**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Update all required boxes</br>4) Click <b>Save</b>|4) Admin user is redirected to the list of videos. Videos are saved with all information and appear at the top of the list in <b>Unpublished</b> state|

### **#5. Verify that the Comments section can be hidden for the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video</br>- The <b>Comments</b> section is shown for video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Click the <b>Comments: Show</b> toggle</br>4) Click <b>Save</b>|3) <b>Comments:</b> changes to <b>Hide</b></br>4) The video is saved with the hidden <b>Comments</b> section|

### **#6. Verify that the Comments section can be shown for the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There is an unpublished video</br>- The <b>Comments</b> section is hidden for video|1) Hover over an unpublished video</br>2) Click "<b>...</b>" button > <b>Edit</b> menu item</br>3) Click the <b>Comments: Hide</b> toggle</br>4) Click <b>Save</b>|3) <b>Comments:</b> changes to <b>Show</b></br>4) The video is saved with the shown <b>Comments</b> section|

</details>
