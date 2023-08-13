### Back to [Sports videos on the portal](../../README.md) feature

# Allow admin users to view the list of existing videos

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the list of existing videos

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the list of existing videos</i></b>

Given I am logged in as an admin user

When I select the <b>Video</b> link on the admin side
Then I see the following:
  - The <b>+ New Video</b> button in the upper-right corner of the page
  - A filter by status
  - A search icon
  - Allow sharing toggle
  - The list of blocks – one block per one existing video – where each block has:
    - Video thumbnail on the left side
    - Video title on the right of the thumbnail
    - Status of the video (<b>Published</b> or <b>Unpublished</b>)
  - The scroll bar next to the list of videos

When I scroll the list of the videos
Then I see a list of videos is appended with a new portion of videos

When I select a <b>Published</b> option in the status filter
Then I see only published videos

When I select an <b>Unpublished</b> option in the status filter
Then I see only unpublished videos

When I select <b>All</b> option in the status filter
Then I see all videos

When I click a search icon
Then I see a search field

When I type some text in the field
Then I see the list of videos is refreshed with matching results
(<i>Search can start when the first symbol is entered or when at least 3 symbols are entered</i>)

When I hover over a video
Then I see the ellipsis (...) menu icon in the upper-right corner

When I click "..." the menu icon for published video
Then I see the following options:
  - <b>Unpublish</b>
  - <b>Delete</b>

When I click "..." the menu icon for unpublished video
Then I see the following options:
  - <b>Publish</b>
  - <b>Edit</b>
  - <b>Delete</b>

When I click the <b>Allow to share videos: Yes</b> toggle
Then the toggle changed to <b>No</b>
  And users can not see the share button on videos

When I click the <b>Allow to share videos: No</b> toggle
Then the toggle changed to <b>Yes</b>
  And users can see and use the share button on videos

<i>You have two options to render a big list: use pagination or infinite scroll</i>

</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Video</b> page
2. Admin user clicks status filter and sees the options
3. Admin user clicks a search icon and sees an input field
4. Admin user sees actions for the published video

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Video page:**

![Admin user sees the Video page](/sports_hub_portal/desktop_application_features/video_page/images/video_index_page.png)

**2. Admin user clicks status filter and sees the options:**

![Admin user clicks status filter and sees the options](/sports_hub_portal/desktop_application_features/video_page/images/status_filter_options.png)

**3. Admin user clicks a search icon and sees an input field:**

![Admin user clicks a search icon and sees an input field](/sports_hub_portal/desktop_application_features/video_page/images/search_field.png)

**4. Admin user sees actions for the published video:**

![Admin user sees actions for the published video](/sports_hub_portal/desktop_application_features/video_page/images/video_actions.png)

</details>

## Test cases

1. Verify the content of the <b>Video</b> page
2. Verify that list of videos is updated according to the selected filter in the status filter
3. Verify that list of videos is populated with new elements when it is scrolled down
4. Verify that admin is able to hide sharing option for videos
5. Verify that admin is able to unhide sharing option for videos
6. Verify that list of videos is updated according to a search match

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Video page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Examine the <b>Video</b> page|1) There are blocks of videos where each block has:</br>- Video thumbnail on the left side</br>- Video title on the right from the thumbnail</br>- Status of the video (<b>Published/Unpublished</b>)|

### **#2. Verify that list of videos is updated according to the selected filter in the status filter**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) In the status filter, select the <b>Published</b> option</br>2) Check if the list with videos is updated</br>3) In the status filter, select the <b>Unpublished</b> option</br>4) Check if the list with videos is updated</br>5) In the status filter, select the <b>All</b> option</br>6) Check if the list with videos is updated|2) Only published videos are shown</br>4) Only unpublished videos are shown</br>6) All videos are shown|

### **#3. Verify that list of videos is populated with new elements when it is scrolled down**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- There are a lot of videos to load|1) Move through the list of videos</br>2) Check if the videos list is loaded|2) When an admin moves through the list of videos, the videos are loaded|

### **#4. Verify that admin is able to hide sharing option for videos**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) <b>Allow to share videos: Yes</b> toggle|1) The toggle changed to <b>No</b>. The <b>Share</b> button is not shown for videos when users browse them|

### **#5. Verify that admin is able to unhide sharing option for videos**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page</br>- The share option is hidden|1) <b>Allow to share videos: No</b> toggle|1) The toggle changed to <b>Yes</b>. The <b>Share</b> button is shown for videos when users browse them|

### **#6. Verify that list of videos is updated according to a search match**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Video</b> page|1) Click a search icon</br>2) Type some text to the field|1) An input field appears</br>2) The list of videos is updated with match|

</details>
