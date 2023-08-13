### Back to [Sports videos](../../README.md) feature

# Allow users to view videos in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to able to view sports news videos

## Acceptance criteria

<pre>
<b><i>Scenario: A user views sports news videos</i></b>

Given I am a user

When I view the <b>Video</b> page
Then I see the following:
  - "Video" header
  - Block of 5 video thumbnails with titles
  - Most Popular section
  - Most Commented section
  - Banners

When I tap the <b>Show more</b> button
Then next 5 videos are loaded

When all videos are loaded
Then the <b>Show more</b> button is not shown anymore

When I tap the <b>Play</b> button on any video
Then I am taken to the video page

When I tap any video thumbnail
Then I am taken to the video page

When I am on the <b>Video</b> page
Then I see the following:
  - The <b>Back</b> button
  - Search icon
  - Video with the <b>Play</b> button
  - Share icon
  - Title under the video
  - Number of views
  - Date of publish
  - Comments section under the video content (Comments functionality is described in separate feature)
  - <b>More video</b> section with the <b>Show more</b> button
  - Banners

When I tap <b>Play</b> button on the <b>Video</b> page
Then I see video starts playing

When I view <b>More video</b> section and tap the <b>Show more</b> button
Then next 5 videos are loaded

When all videos are loaded
Then the <b>Show more</b> button is not shown in <b>More video</b> section
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Video</b> in the navigation menu
2. Users see <b>Video</b> list page
3. Users see <b>Show more</b> button on video list page
4. Users see <b>Video</b> page
5. Users see <b>Show more</b> button in <b>More video</b> section
6. Full video list page
7. Full video view page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Video in the navigation menu:**

![Users see Video in the navigation menu](/sports_hub_portal/mobile_application_features/video_page/images/application_navigation_menu.png)

**2. Users see Video list page:**

![Users see Video list page](/sports_hub_portal/mobile_application_features/video_page/images/application_video_list_page.png)

**3. Users see Show more button on video list page:**

![Users see Show more button on video list page](/sports_hub_portal/mobile_application_features/video_page/images/application_show_more_button.png)

**4. Users see Video page:**

![Users see Video page](/sports_hub_portal/mobile_application_features/video_page/images/application_video_view_page.png)

**5. Users see Show more button in More video section:**

![Users see Show more button in More video section](/sports_hub_portal/mobile_application_features/video_page/images/application_show_more_more_video_section.png)

**6. Full video list page:**

![Full video list page](/sports_hub_portal/mobile_application_features/video_page/images/video_list_page.png)

**7. Full video view page:**

![Full video view page](/sports_hub_portal/mobile_application_features/video_page/images/video_view_page.png)

</details>

## Test cases

1. Verify the content of the <b>Video</b> page in the <b>Sports Hub</b> application
2. Verify that 5 more videos are loaded by tapping the <b>Show more</b> button
3. Verify that the <b>Show more</b> button is not shown in case there are no more videos to load
4. Verify redirection to the <b>Video</b> page by tapping the <b>Play</b> button
5. Verify redirection to the <b>Video</b> page by tapping the video thumbnail
6. Verify the content of the <b>Video</b> page
7. Verify ability to play video on the <b>Video</b> page
8. Verify that 5 more videos are loaded in <b>More videos</b> section by tapping the <b>Show more</b> button
9. Verify that the <b>Show more</b> button is not shown in <b>More video</b> section in case there are no more videos to load
10. Verify the <b>Back</b> button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Video page in the Sports Hub application**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page|1) Observe the page|1) The <b>Video</b> page contains the following:</br>- "Video" header</br>- Search icon</br>- Block of five video thumbnails with titles</br>- The <b>Show more</b> button</br>- Most Popular section</br>- Most Commented section</br>- Banners|

### **#2. Verify that 5 more videos are loaded by tapping the Show more button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are more than 10 videos|1) Go to the <b>Video</b> page</br>2) Tap the <b>Show more</b> button|2) Next 5 videos are loaded|

### **#3. Verify that the Show more button is not shown in case there are no more videos to load**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are more than 5 but less than 10 videos|1) Go to the <b>Video</b> page</br>2) Tap the <b>Show more</b> button|2) Next videos are loaded. The <b>Show more</b> button is not shown|

### **#4. Verify redirection to the Video page by tapping the Play button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page|1) Tap the <b>Play</b> button for any video|1) The user is redirected to the <b>Video</b> page|

### **#5. Verify redirection to the Video page by tapping the video thumbnail**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page|1) Tap the thumbnail|1) The user is redirected to the <b>Video</b> page|

### **#6. Verify the content of the Video page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Video</b> page|1) Examine the <b>Video</b> page|1) The <b>Video</b> page contains the following:</br>- The <b>Back</b> button</br>- Search icon</br>- Video with the <b>Play</b> button</br>- <b>Share</b> icon below the video</br>- Title under the video</br>- Number of views</br>- Date of publish</br>- Comments section under the video content</br>- <b>More video</b> section with the <b>Show more</b> button</br>- Banners|

### **#7. Verify ability to play video on the Video page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Video</b> page|1) Tap the <b>Play</b> button</br>2) Tap the video|1) The video starts playing</br>2) The video pauses|

### **#8. Verify that 5 more videos are loaded in More videos section by tapping the Show more button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Video</b> page</br>- There are more than 10 videos|1) Tap the <b>Show more</b> button in the <b>More videos</b> section|1) Next 5 videos are loaded|

### **#9. Verify that the Show more button is not shown in More video section in case there are no more videos to load**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Video</b> page</br>- There are more than 5 but less than 10 videos|1) Tap the <b>Show more</b> button|1) Next videos are loaded. The <b>Show more</b> button is not shown|

### **#10. Verify the Back button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Video</b> view page|1) Tap the <b>Back</b> button|1) The user is redirected to the <b>Video</b> list page|

</details>
