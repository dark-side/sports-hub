### Back to [Sports videos on the portal](../../) feature

# Allow admin users to add new videos

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to add new videos

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user add a new video</i></b>

Given I am logged in as an admin user

When I select the <b>Video</b> link on the admin side 
Then I see the <b>+ New Video</b> button in the upper-right corner of the page

When I click the <b>+ New Video</b> button
Then I see the pop-up window appears with input for the video link, input to upload video, the <b>Cancel</b> and <b>Add</b> buttons

When I enter a video link and click <b>Add</b>
Then I see a new video is added and the page contains:
  - Play and pause the video, enter a full-screen video mode, configure video volume and video settings
  - <b>Video</b> title field
  - The <b>Preview</b> icon in the upper-right corner of the page
  - The <b>Comments Show/Hide</b> toggle
  - <b>Cancel</b> and <b>Save</b> buttons in the upper-right corner of the page (the <b>Save</b> button is disabled till required fields are not filled in)

When I click the <b>Preview</b> icon
Then I see how this video page is shown for the users
  And I see <b>Back to edit page</b> link

When I select <b>Back to edit page</b> link
Then I am taken back to edit video page

When I enter the title and I click the <b>Save</b> button
Then I see the page with a list of the videos
  And I see that my video is added at the top of the list in <b>Unpublished</b> state

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I click to confirm
Then I see the page with a list of the videos
  And the video is not saved

When I click the <b>Comments: Hide</b> toggle
Then the toggle changed to <b>Show</b>
  And <b>Comments</b> section is shown for users

When I click the <b>Comments: Show</b> toggle
Then the toggle changed to <b>Hide</b>
  And <b>Comments</b> section is not shown for users

When I hover over the video field
Then I see the <b>Delete</b> icon appears

When I click the <b>Delete</b> icon
Then I see a confirmation dialog

When I click <b>Cancel</b>
Then I see the dialog disappears and video is still present

When I click <b>Delete</b>
Then I see the "The video is successfully deleted" flash message

When I hover over the video field
Then I see the <b>Add new video</b> icon appears
  And can be used to upload another video
</pre>

## Mockups

1. Admin user clicks the <b>+ New Video</b> button and sees a pop-up window
2. Admin user sees a new video form
3. Admin user hovers over uploaded video
4. Admin user sees a success save flash message
5. Admin user sees a delete confirmation dialog
6. Admin user sees a cancel confirmation dialog
7. Admin user sees a video preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user clicks the + New Video button and sees a pop-up window:**

![Admin user clicks the + New Video button and sees a pop-up window](/products/sport_news_portal/web_application_features/video_page/images/new_video_popup.png)

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

1. Verify that admin is able to add a video
2. Verify that admin is not able to save a new video when required fields are not filled
3. Verify that admin is able to preview a new video
4. Verify that the <b>Comments</b> section can be hidden for a new video
5. Verify that the <b>Comments</b> section can be shown for a new video

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to add a video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Click <b>+ New Video</b></br>2) Enter a video link and click <b>Add</b></br>3) Fill in the title field</br>4) Click <b>Save</b>|4) Admin user is redirected to the list of videos. The video is saved and appears at the top of the list in <b>Unpublished</b> state|

### **#2. Verify that admin is not able to save a new video when required fields are not filled**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Click <b>+ New Video</b></br>2) Enter a video link and click <b>Add</b></br>3) Do not fill in the <b>Video title</b> required field</br>4) Click <b>Save</b></br>5) Delete the video</br>6) Fill in the <b>Video title</b> required field</br>7) Click <b>Save</b>|4) The required fields are highlighted in red. The validation message "Fill in all required fields" appears</br>7) The required fields are highlighted in red. The validation message "Fill in all required fields" appears|

### **#3. Verify that admin is able to preview a new video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Click <b>+ New Video</b></br>2) Upload video</br>3) Enter title</br>4) Click the <b>Preview</b> icon</br>5) Select <b>Back to edit page</b> link|4) The video is shown as it will appear for users</br>5) The video is back to edit mode|

### **#4. Verify that the Comments section can be hidden for a new video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Click <b>+ New Video</b></br>2) Upload video</br>3) Enter title</br>4) Click the <b>Comments: Show</b> toggle</br>5) Click <b>Save</b>|4) The <b>Comments</b> toggle changes to <b>Hide</b></br>5) The video is saved but the <b>Comments</b> section is not shown for users|

### **#5. Verify that the Comments section can be shown for a new video**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Click <b>+ New Video</b></br>2) Upload video</br>3) Enter title</br>4) The <b>Comments</b> toggle is in <b>Show</b> state</br>5) Click <b>Save</b>|5) The video is saved with the <b>Comments</b> section shown for users|

</details>
