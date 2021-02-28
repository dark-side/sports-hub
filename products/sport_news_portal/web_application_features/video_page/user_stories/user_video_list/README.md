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

When I view the <b>Video</b> page on the Sports Hub site
Then I see the following:
  - The main video at the top of the main content area with the <b>More</b> button in the upper-right corner of the main video
  - The scrollable block of four video thumbnails with a video title

When I click the <b>Play</b> button on the main video
Then I see the video starts playing

When I click the <b>More</b> button at the top right corner of the main video
Then I am taken to the video page

When I click the non-main video thumbnail
Then I am taken to the <b>Video</b> page

When I am on the video page
Then I see the following:
  - Video
  - The <b>Share</b> button if sharing is enabled
  - The title under the video
  - Number of views
  - Date of publish
  - The <b>Comments</b> section under the article content if enabled
  - More videos section under the <b>Comments</b> section
</pre>

## Mockups

1. Users see a video list page
2. Users see a video view page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a video list page:**

![Users see a video list page](/products/sport_news_portal/web_application_features/video_page/images/user_video_list_page.png)

**2. Users see a video view page:**

![Users see a video view page](/products/sport_news_portal/web_application_features/video_page/images/user_video_view_page.png)

</details>

## Test cases

1. Verify the content of the <b>Video</b> page on the Sports Hub site
2. Verify redirection to the <b>Video</b> page by clicking the <b>More</b> button
3. Verify redirection to the <b>Video</b> page by clicking the video thumbnail

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Video page on the Sports Hub site**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page on the Sports Hub site|1) Observe the page|1) The <b>Video</b> page contains the following:</br>- The main video at the top of the main content area with the <b>More</b> button at the top right corner of a video</br>- The scrollable block consisting of four video thumbnails with video titles|


### **#2. Verify redirection to the Video page by clicking the More button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page on the Sports Hub site|1) In the upper-right corner of the main video, click <b>More</b>|1) The user is redirected to the <b>Video</b> page|

### **#3. Verify redirection to the Video page by clicking the video thumbnail**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Video</b> page on the Sports Hub site|1) Click non-main videos thumbnail|2) The user is redirected to the <b>Video</b> page|

</details>
