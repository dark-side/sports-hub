### Back to [Sports videos on the portal](../../) feature

# Allow admin users to edit an existing video

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to edit an existing unpublished video

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits the existing unpublished video</i></b>

Given I am logged in as an admin user

When I click the <b>Videos</b> link on the admin side
Then I see the list of blocks with videos

When I hover over an unpublished video
Then I see the ellipsis (...) button in the upper-right corner

When I click "..." the menu icon for unpublished video
Then I see the Edit menu item present

When I select Edit menu item
Then I see a pre-populated form with video details:
  - Play and pause the video, enter a full-screen video mode, configure video volume and video settings
  - <b>Video</b> title field
  - <b>Preview</b> icon in the upper-right corner of the page
  - <b>Comments Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> buttons in the upper-right corner of the page (<b>Save</b> disabled until any changes are made)

When I click the Preview link button
Then I see how this video is shown for users.

When I make any changes in the form
Then I see the <b>Save</b> button is enabled

When I click the <b>Save</b> button
Then I see the page with a list of the videos
  And I see that my updated video appears at the top of the list in <b>Unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I click Confirm
Then I see the page with a list of the videos
  And changes to the video are not saved
</pre>

## Mockups

1. Admin user clicks to upload new video on the edit page and sees a popup
2. Admin user sees a video form
3. Admin user hovers over uploaded video
4. Admin user sees a success save flash message
5. Admin user sees a delete confirmation dialog
6. Admin user sees a cancel confirmation dialog
7. Admin user sees a video preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user clicks the + New Video button and sees a popup:**

![Admin user clicks the + New Video button and sees a popup](/products/sport_news_portal/web_application_features/video_page/images/new_video_edit_popup.png)

**2. Admin user sees a new video form:**

![Admin user sees a new video form](/products/sport_news_portal/web_application_features/video_page/images/video_form.png)

**3. Admin user hovers over uploaded video:**

![Admin user hovers over uploaded video](/products/sport_news_portal/web_application_features/video_page/images/hover_over_video.png)

**4. Admin user sees a success save flash message:**

![Admin user sees a success save flash message](/products/sport_news_portal/web_application_features/video_page/images/success_save_message.png)

**5. Admin user sees a delete confirmation dialog:**

![Admin user sees a delete confirmation dialog](/products/sport_news_portal/web_application_features/video_page/images/delete_confirmation.png)

**6. Admin user sees a cancel confirmation dialog:**

![Admin user sees a cancel confirmation dialog](/products/sport_news_portal/web_application_features/video_page/images/cancel_confirmation.png)

**7. Admin user sees a video preview page:**

![Admin user sees a video preview page](/products/sport_news_portal/web_application_features/video_page/images/video_preview.png)

</details>

## Test cases

1. Verify that admin is able to change a video to the edited video
2. Verify that admin is not able to save empty required fields to the edited video
3. Verify that admin is able to preview the edited video
4. Verify that admin is able to save the edited video with all valid data updated
5. Verify that the comments section can be hidden for the edited video
6. Verify that the comments section can be shown for the edited video

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to change a video to the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) In the video section, click <b>Add new video</b></br>4) Enter a video link and click <b>Add</b></br>5) Click <b>Save</b> button|5) Admin user is redirected to the list of videos. Video is saved with all information and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to save empty required fields to the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) In the <b>Video Title</b> required field delete data</br>4) Click <b>Save</b> button</br>5) Fill in the <b>Video Title</b> required field</br>6) Hover over the video</br>7) Click <b>Delete</b> icon</br>8) Click <b>Save</b>|4) The required fields are highlighted in red. The validation message "Fill in all required fields" is shown</br>8) The required fields are highlighted in red. The validation message "Fill in all required fields" is shown|

### **#3. Verify that admin is able to preview the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Make some changes</br>4) Click the <b>Preview</b> link</br>5) Click <b>Back to edit page</b> link|4) The video is shown as it will look for users</br>5) The video is back to edit mode|

### **#4. Verify that admin is able to save the edited video with all valid data updated**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Update all required boxes</br>4)Click <b>Save</b> button|4) Admin user is redirected to the list of videos. Videos are saved with all information and appear at the top of the list in <b>Unpublished</b> state|

### **#5. Verify that the comments section can be hidden for the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video</br>- Comments section is shown for video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Click the <b>Comments: Show</b> toggle</br>4)Click <b>Save</b> button|3) <b>Comments:</b> changed to <b>Hide</b></br>4) The video is saved with the hidden comments section|

### **#6. Verify that the comments section can be shown for the edited video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to <b>Videos</b> page</br>- There is an unpublished video</br>- Comments section is hidden for video|1) Hover over an unpublished video</br>2) Click "..." button -> <b>Edit</b> menu item</br>3) Click the <b>Comments: Hide</b> toggle</br>4)Click <b>Save</b> button|3) <b>Comments:</b> changed to <b>Show</b></br>4) The video is saved with the shown comments section|

</details>
