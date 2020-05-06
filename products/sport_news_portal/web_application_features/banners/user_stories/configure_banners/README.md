### Back to [Banners on the portal](/../../) feature

# Allow users to configure banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user 
    I want to be able to configure list of Banners
	So that users can see them while view the Sport News site

## Acceptance criteria

    Scenario: An admin user configures list of Banners
    Given I am logged in as an admin user

    When I view a Banners configuration page
    Then I see a following:
	  1. Two tabs with list of banners - Open tab and Closed tab with count of available banners displayed next to the tab name
      2. Section with a Banner label and the Add Banner button under the header section
    When I view the Open tab
    Then I see a table with a list of open banner names, banner status and a category in which this banner should be displayed 
      And I am able change banner status from Not Published to Published and from Published to Closed
    When I change banner status to Published
    Then I see a banner appears at the main site pages related to the banner’s category
    When I change banner category 
    Then I see it is displayed only on those pages in the main site that are related to specified category
    Note: Banner should be displayed on subcategories and team pages that are related to the banner’s category 
    When I select any banner from the table
    Then I see a banner preview block at the right side of the page with a banner photo
    When I select Published banner
    Then I see a publish date of the banner in the preview block
    When I select Unpublished banner
    Then I see a last update date of the banner and Edit and Delete buttons in the preview block
    When I click on Edit button
    Then I see a Add picture icon and banner name input appear with Save and Delete buttons
    When I click on the Add picture icon
    Then I am able to upload a new banner photo
    When I delete a banner’s photo and save the banner
      And I select Publish option in Status column
    Then I see a validation message that I cannot publish banner without a photo
    When I delete a banner name and click Save button
    Then I see a validation that banner name must be present
    When I click on Add new banner button
    Then I see a dialog with name input and Cancel and Save buttons appears
    When I fill in the banner name and click Save button
    Then I see a banner is displayed at the top of the banners table with Not Published status and a fist category from the categories list
    When I click on this new banner in the table list
    Then I see a banner photo preview block is opened at the right side of the page with Add picture icon and Edit and Delete buttons
    When I view the Closed tab
    Then I see a table with a list of closed banner names, close date, and category it was published in
    When I select any banner from the table
    Then I see a banner preview block at the right side of the page with a banner photo
    When I hover over the banner on the table
    Then I see a Delete icon appears at the right of the banner row
    When I click on the Delete icon
    Then I see a banner is deleted

## Mockups

1. User sees Banners configuration page
2. User sees closed banners list
3. User sees New banner popup
4. User sees published banner
5. User sees recently added banner
6. User sees unpublished banner

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Banners configuration page:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/banners_configuration_page.png)

**2. User sees closed banners list:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/closed_banners.png)

**3. User sees New banner popup:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/new_banner_popup.png)

**4. User sees published banner:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/published_banners.png)

**5. User sees recently added banner:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/recently_added_banner.png)

**6. User sees unpublished banner:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/unpublished_banners.png)

</details>

## Test Scenarios

1. Verify the content of the Banners configuration page
2. Verify the content of Open tab of the Banners configuration page
3. Verify changing of banner status on the Banners configuration page
4. Verify banner preview block on the Banners configuration page
5. Verify that admin can upload a new banner photo
6. Verify deleting banner’s photo on the Banners configuration page
7. Verify adding new banner on the Banners configuration page
8. Verify deleting banner on the Banners configuration page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|
|4|Observe the content of the Banners configuration page|The content of the Banners configuration page consists of:<br> - Two tabs with list of banners - Open tab and Closed tab with count of available banners displayed next to the tab name<br> - Section with a Banner label and the Add Banner button under the header section


### **#2. Verify the content of Open tab of the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|The list of articles below the comments section including:<br> - Heading "More Articles"<br> - Article thumbnail photo<br> - Article Headline<br> - Article Summary/Excerpt
|4|Observe the content of the Banners configuration page|The content of the Banners configuration page consists of:<br> - Two tabs with list of banners - Open tab and Closed tab with count of available banners displayed next to the tab name<br> - Section with a Banner label and the Add Banner button under the header section
|5|Check the content of Open tab|There is a  table with a list of open banner names, banner status and a category in which this banner should be displayed


### **#3. Verify changing of banner status on the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|
|4|Check the content of Open tab|There is a  table with a list of open banner names, banner status and a category in which this banner should be displayed
|5|Click on dropdown menu near Not Published status and choose Publish|Not Published status is changed to Publish
|6|Click on dropdown menu near Published status and choose Close|The banner appears at the main site pages related to the banner’s category

### **#4. Verify banner preview block on the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|
|4|Check the content of Open tab|There is a  table with a list of open banner names, banner status and a category in which this banner should be displayed
|5|Сlick on Banner|The banner preview block is opened at the right side of the page with a banner photo and a Delete and Edit photo buttons and a published date (if banner status is active)

### **#5. Verify that admin can upload a new banner photo**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|
|4|Check the content of Open tab|There is a  table with a list of open banner names, banner status and a category in which this banner should be displayed
|5|Сlick on Banner|The banner preview block is opened at the right side of the page with a banner photo and a Delete and Edit photo buttons and a published date (if banner status is active)
|6|Сlick Edit|The Add picture icon appears with Select and Delete buttons
|7|Click on the Add picture icon|Admin is able to upload a new banner photo

### **#6. Verify deleting banner’s photo on the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|
|4|Check the content of Open tab|There is a  table with a list of open banner names, banner status and a category in which this banner should be displayed
|5|Сlick on Banner with active status|The banner preview block is opened at the right side of the page with a banner photo and a Delete and Edit photo buttons and a published date (if banner status is active)
|6|Click on Delete button near banner photo|Banner’s photo is deleted

### **#7. Verify adding new banner on the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Banners icon on the left side bar|
|4|Click on New Banner button|The dialog with name input and Cancel and Save buttons appear
|5|Fill in the banner name|
|6|Click Save button|Then the new banner is displayed at the top of the banners table with Not Published status and a fist category from the categories list

### **#8. Verify deleting banner on the Banners configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Closed tab|
|4|Observe the content of Closed tab|There is a table with a list of closed banner names and date when the banner status was changed to closed
|5|Hover over the banner on the table|The Delete icon appears at the right of the banner row
|6|Click on the Delete icon|The banner is deleted

</details>

