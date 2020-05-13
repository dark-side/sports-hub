### Back to [Manage Advertisements on the portal](/../../) feature

# Allow admin user to configure Advertisements

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to configure list of Advertisements  
    So that it is possible to promote products via the Sport News site

## Acceptance criteria

    Scenario: An admin site configures list of Advertisements 
    Given I am logged in as an admin user

    When I view an Ads configuration page
    Then I see the following:
      - Table with list of available advertisements that contains the following headers: ads name, status, actions
      - Section with an Advertisements label and the Add Ads button under the header section 
    When I click on the Add Adds button
    Then I see the modal with an input for new ads name and a Cancel/Save buttons
    When I fill in new ads name and click save button
    Then I see new ads is added in the top of the Ads table, Ads preview block is displayed at the right side of the page with a date of Ads creation and a configuration form is opened with:
      - URL Input for advertised item 
      - List of categories where advertisement should be displayed (Note: advertisement category is optional. If no category is selected, then advertisement can be shown at any page of the site)
      - Opened (number that indicates how many times user clicked on the advertised item, defaults to 0 for new advertisement)
      - Displayed (number that indicates how many times advertisement is displayed on the site, defaults to 0 for new advertisement)
      - Cancel/Save buttons
    When I fill in advertisement URL
    Then I see a advertisement image in the preview block at the right side of the page
    When I check some category for the advertisement and click a Save button
    Then I see this advertisement only on those pages in the main site that are related to specified category
    When I don't check any category
    Then I see this advertisement at any page of the site
    When I click on any advertisement on the table
    When I change advertisement status from Inactive to Active 
    Then I see an advertisement on the Sport News site
    When I change advertisement status from Active to Inactive
    Then I do not see Ads are displayed on the Sport News site
    When I click on Edit advertisement icon
    Then the form with advertisement details is opened and I can edit advertisement
    When I click on the Delete icon
    Then I see a advertisement is deleted

## Mockups

1. User sees Empty Page message
2. User sees Add new Ads popup
3. User sees Add new Ads empty form
4. User sees Add new Ads filled in form
5. User sees Ads is added popup
6. User sees Ads list table

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Empty Page message:**

![Empty Page Screen](/products/sport_news_portal/web_application_features/manage_ads/images/no_ads_added.png)

**2. User sees Add new Ads popup:**

![Add new Ads popup](/products/sport_news_portal/web_application_features/manage_ads/images/add_new_ads_popup.png)

**3. User sees Add new Ads empty form**

![New Ads empty form Screen](/products/sport_news_portal/web_application_features/manage_ads/images/add_new_ads.png)

**4. User sees Add new Ads filled in form**

![New Ads filled in form Screen](/products/sport_news_portal/web_application_features/manage_ads/images/add_new_ads_filled_in_form.png)

**5. User sees Ads is added popup**

![Ads is added popup](/products/sport_news_portal/web_application_features/manage_ads/images/ads_is_saved_popup.png)

**6. User sees Ads list table**

![Ads list Screen](/products/sport_news_portal/web_application_features/manage_ads/images/ads_list.png)


</details>

## Test Scenarios

1. Verify the content of the Advertising configuration page
2. Verify changing advertisement status from Inactive to Active
3. Verify clicking on an advertisement 
4. Verify clicking on +New Ads button
5. Verify clicking on Delete button
6. Verify Active to Inactive status change on the Advertising configuration page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of the Advertising configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the Sport News site|
|2|Log in your admin account|
|3|Navigate to Advertising configuration page|
|4|Observe the content of the page|Such elements should be present:<br>- Table with the following headers: Ads Name, Status, Actions<br>- Section with an Advertisements label and the Add Advertisement button under the header section 

### **#2. Verify changing advertisement status from Inactive to Active**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the Sport News site|
|2|Log in your admin account|
|3|Navigate to Advertising configuration page|
|4|Сhange advertisement status from Inactive to Active|Advertisement is shown on the main site

### **#3. Verify clicking on an advertisement**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the Sport News site|
|2|Log in your admin account|
|3|Navigate to Advertising configuration page|
|4|Click on any Advertisement on the table|The advertisement image preview block is opened at the right side of the page with an advertisement photo and a created date

### **#4. Verify clicking on +New Ads button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the Sport News site|
|2|Log in your admin account|
|3|Navigate to Advertising configuration page|
|4|Click on +New Ads button|The dialog with name input and Cancel and Save buttons appear
|5|Fill in the Advertisement name|The new advertisement is displayed at the top of the advertisements table with Inactive status 

### **#5. Verify clicking on Delete button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the Sport News site|
|2|Log in your admin account|
|3|Navigate to Advertising configuration page|
|4|Click on Delete button near any Ad from the list|The advertisement is deleted

### **#6. Verify Active to Inactive status change on the Advertising configuration page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the Sport News site|
|2|Log in your admin account|
|3|Navigate to Advertising configuration page|
|4|Сhange advertisement status from Active to Inactive|Ad is not displayed on the Sport News site

</details>
