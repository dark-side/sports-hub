### Back to [Video Page of the portal](/../../) feature

# Allow users to see Video page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to able to view sport news videos
    So that I can view sport matches, news, etc

## Acceptance criteria

    Scenario: A site user views sport news videos
    Given I am logged in as a site user

    When I view the Videos page of the Sport News site
    Then I see the following:
      - a main video at the top of the main content area with a More button at the top right corner of a video
      - a scrollable block of four (depending on the CMS configuration) video thumbnails with video title
    When I click on the play video button for the main video
    Then I see the video is played
    When I click on the More button at the top right corner of the main video
    Then I am taken to the video article page
    When I click on the video thumbnail of the
    Then I am taken to the video article page

## Mockups

1. User sees Video page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Video page:**

![Video page Screen](/products/sport_news_portal/web_application_features/video_page/images/video_page.png)

</details>

## Test Scenarios

1. Verify the content of the Video page of the Sport News site
2. Verify clicking on the More button for the main video
3. Verify clicking on the thumbnail button for the main video
4. Verify clicking on the play button on the main video

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of the Video page of the Sport News site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Go to Video page of the Sport News site|The Video page should contain:<br>- a main video at the top of the main content area with a More button at the top right corner of a video<br>- a scrollable block of four (depending on the CMS configuration) video thumbnails with video title

### **#2. Verify clicking on the More button for the main video**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Go to Video page of the Sport News site|
|4|Click on More button at the top right corner of the main video|User is taken to the video article page

### **#3. Verify clicking on the thumbnail button for the main video**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Go to Video page of the Sport News site|
|4|Click on thumbnail button|User is taken to the video article page

### **#3. Verify clicking on the play button on the main video**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Go to Video page of the Sport News site|
|4|Click on play button on the main video|The video is played

</details>
