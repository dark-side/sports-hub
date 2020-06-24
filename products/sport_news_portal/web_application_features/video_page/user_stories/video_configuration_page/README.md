### Back to [Video Page of the portal](../../) feature

# Allow admin users to configure Video page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to able to configure the videos available on the Video page page as well as the page structure
    So that I have control over what users can see when access the Video page

## Acceptance criteria

    Scenario: An admin user configures the videos available on the Video page page as well as the page structure
    Given I am logged in as an admin user

    When I am on video configuration page
    Then I see the following:
      - Video title and a Cancel and a Save buttons located in the section between the site header and horizontal navigation
      - Page preview button
      - Add new main video uploader with a video title input
      - Section with two columns containing two videos per column and video title input
      - Most popular section with a toggle to show/hide this section
      - Most commentable section with a toggle to show/hide this section
    When I click on the Add new video icon for a main page video section
    Then I see the dialog window with an input for video link and Save and Cancel buttons is opened
    When I fill in a video link input and click a save button
    Then I see a new video from Youtube is linked to a Sport News site
      And I see a play/pause the video, enter a full-screen video mode, configure video volume and video settings
    When I fill in a video title input (note that the video title input is disabled until the Add new video icon is clicked and Youtube video link is provided)
      And move down the page to configure the two-columns section with the videos
    Then I see a link four more videos from the Youtube in the same way as is described above for the main video (Note: if video don’t have either video title or video link, then such video is not displayed on the main site)
    When I toggle an option show the Most Popular section
      And I click the Save page configuration button
    Then I see the Most Popular column containing three articles with the highest number of views on the Video page of the Sport News site
    When I toggle an option hide the Most Popular section
      And I click the Save page configuration button
    Then I do not see the display of Most Popular column on the Video page of the Sport News site
    When I toggle an option show the Most Comentabe section
      And I click the Save page configuration button
    Then I see the Most Comentabe column containing three articles with the highest number of comments on the Video page of the Sport News site
    When I toggle an option hide the Most Comentabe section
      And I click the Save page configuration button
    Then I do not see the display of Most Comentabe column on the Video page of the Sport News site
    When I click on the Preview page button at the top right of the page
    Then I see how Video page would look like on the main Sport News site
    When I preview the page
    Then I can not play the video or click any buttons, access menu, etc
      And I am able view page layout
      And I see a Preview indicator at the top right side of the page content
    When I update any of the video page configuration
      And I click a cancel button
    Then I see a changes applied to the Video page configuration are not saved

## Mockups

1. User sees video configuration page with not uploaded videos
2. User sees video configuration page with uploaded videos
3. User sees video upload popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees video configuration page with not uploaded videos:**

![Video configuration page with not uploaded videos Screen](/products/sport_news_portal/web_application_features/video_page/images/video_configuration_empty_videos.png)

**2. User sees video configuration page with uploaded videos:**

![Video configuration page with uploaded videos Screen](/products/sport_news_portal/web_application_features/video_page/images/video_configuration_page.png)

**3. User sees video upload popup:**

![Video upload popup Screen](/products/sport_news_portal/web_application_features/video_page/images/video_upload.png)

</details>

## Test Scenarios

1. Verify the content of video configuration page
2. Verify adding new video from YouTube to a Sport News site
3. Verify that user can play/pause the video on the Sport News site
4. Verify that user can play video in full-screen video mode on the Sport News site
5. Verify that user can change the volume of the video on the Sport News site
6. Verify toggle an option show the Most Popular section
7. Verify toggle an option hide the Most Popular section
8. Verify toggle an option show the Most Commentable section
9. Verify toggle an option hide the Most Commentable section
10. Verify the preview button on the video configuration page
11. Verify the video title can be edited on the video configuration page
12. Verify the video title edit can be canceled on the video configuration page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of video configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Observe the content of video configuration page|There should be the following components:<br>- Video title and a Cancel and a Save buttons located in the section between the site header and horizontal navigation<br>– Page preview button<br>- Add new main video uploader with a video title input<br>- Section with two columns containing two videos per column and video title input<br>- Most popular section with a toggle to show/hide this section<br>- Most commentable section with a toggle to show/hide this section

### **#2. Verify adding new video from YouTube to a Sport News site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Click on the Add new video icon for a main page video section|Then the dialog window with an input for video link and Save and Cancel buttons is opened
|5|Fill in a video link input|
|6|Click a save button|The new video from Youtube is linked to a Sport News site

### **#3. Verify that user can play/pause the video on the Sport News site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Chose any video from the page and tap on play button|The video starts playing with no issues
|5|Stop the video|The video is stooped
|6|Start playing it again|The video start playing again

### **#4. Verify that user can play video in full-screen video mode on the Sport News site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Chose any video from the page and tap on play button|The video starts playing with no issues
|5|Open video in full screen mode and start playing it|Video is played with no issues in a full-screen mode
|6|Go back from the open screen mode|Video come back to default size successfully

### **#5. Verify that user can change the volume of the video on the Sport News site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Chose any video from the page and tap on play button|The video starts playing with no issues
|5|Increase the volume|The volume is increased
|6|Decrease the volume|The volume is decreased

### **#6. Verify toggle an option show the Most Popular section**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Toggle an option show the Most Popular section|
|5|Click the Save page configuration button|The system displays the Most Popular column containing three articles with the highest number of views on the video page of the Sport News site

### **#7. Verify toggle an option hide the Most Popular section**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Toggle an option hide the Most Popular section|
|5|Click the Save page configuration button|The system does not display the Most Popular column on the video page of the Sport News site

### **#8. Verify toggle an option show the Most Commentable section**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Toggle an option show the Most Commentable section|
|5|Click the Save page configuration button|The system displays the Most Commentable column containing three articles with the highest number of comments on the video page of the Sport News site

### **#9. Verify toggle an option show the Most Commentable section**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Toggle an option show the Most Commentable section|
|5|Click the Save page configuration button|The system displays the Most Commentable column containing three articles with the highest number of comments on the video page of the Sport News site

### **#10. Verify the preview button on the video configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Click on the Preview page button at the top right of the page|Video page would look like on the main Sport News site
|5|Click the Save page configuration button|The system displays the Most Commentable column containing three articles with the highest number of comments on the video page of the Sport News site

### **#11. Verify the video title can be edited on the video configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Click on any video|
|5|Edit a title of a video|
|6|Click Save button|The changes has been saved

### **#12. Verify the video title edit can be canceled on the video configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on video icon on the sidebar|Admin user is redirected to video configuration page
|4|Click on any video|
|5|Edit a title of a video|
|6|Click on Cancel button|The changes are not saved

</details>
