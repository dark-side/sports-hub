### Back to [Sports videos on the portal](../../) feature

# Allow site users to view videos on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to view sports videos

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views sports videos</i></b>

Given I am a site user

When I view the <b>Videos</b> page on the Sport News site
Then I see the following:
  - The main video at the top of the main content area with the More button in the upper-right corner of the main video
  - The scrollable block of four video thumbnails with a video title

When I click the play button on the main video
Then I see the video starts playing

When I click the <b>More</b> button at the top right corner of the main video
Then I am taken to the video page

When I click on the non-main video thumbnail
Then I am taken to the video page

When I am on the video page
Then I see the following:
  - Video
  - Share button if sharing enabled
  - The title under the video
  - Number of views
  - Date of publish
  - The comments section under the article content if enabled
  - More videos section under the comment section
</pre>

## Mockups

1. User sees Video list page
2. User sees a video view page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Video list page:**

![User sees Video list page](/products/sport_news_portal/web_application_features/video_page/images/user_video_list_page.png)

**2. User sees a video view page:**

![User sees a video view page](/products/sport_news_portal/web_application_features/video_page/images/user_video_view_page.png)

</details>

## Test cases

1. Verify the content of the Videos page of the Sport News site
2. Verify redirection to the video page by clicking the More button
3. Verify redirection to the video page by click on the video thumbnail

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Videos page of the Sport News site**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page of the Sport News site|1) Observe the page|1) The Video page contains the following:</br>- The main video at the top of the main content area with a More button at the top right corner of a video</br>- The scrollable block of four video thumbnails with video titles|


### **#2. Verify redirection to the video page by clicking the More button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page of the Sport News site|1) In the upper-right corner of the main video, click <b>More</b>|1) User is redirected to the video page|

### **#3. Verify redirection to the video page by click on the video thumbnail**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page of the Sport News site|1) Click on non-main videos thumbnail|2) User is redirected to the video page|

</details>
