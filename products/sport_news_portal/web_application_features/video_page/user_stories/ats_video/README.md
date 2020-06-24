### Back to [Video Page of the portal](/../../) feature

# Allow users to see ATS Video in the sidebar block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to able to view ATS Video sidebar block
    So that I can quickly view the most recent sport news video

## Acceptance criteria

    Scenario: A site user views ATS Video sidebar block
    Given I am logged in as a site user

    When I view any sport category page with the ATS Video sidebar block
    Then I see the following:
      - Heading "ATS Video"
      - Video thumbnail
      - Video title
    When I click the video block
    Then I am taken to the video article page
      And I see the ATS Video is the most recent video related to the section of the site I am viewing (e.g. show a baseball video when I am in the MLB section of the site) Team

## Mockups

1. User sees page with ATS Video block

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees page with ATS Video block:**

![Page with ATS Video block Screen](/products/sport_news_portal/web_application_features/video_page/images/page_with_ats_video_bblock.png)

</details>

## Test Scenarios

1. Verify the content of sport category page with the ATS Video sidebar block
2. Verify clicking on the ATS Video block
3. Verify that the ATS Video section includes the most recent video related to the section of the site

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of sport category page with the ATS Video sidebar block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on any sport category page with ATS Video sideblock|On opened page should be the following:<br>- Heading "ATS Video"<br>- Video thumbnail<br>- Video title

### **#2. Verify clicking on the ATS video block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on any sport category page with ATS Video sideblock|
|4|Click on ATS sideblock|User is navigating to the video article page

### **#3. Verify that the ATS Video section includes the most recent video related to the section of the site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on any sport category page with ATS Video sideblock|
|4|Observe the ATS sideblock|The ATS Video is the most recent video are related to baseball

</details>
