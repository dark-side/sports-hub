### Back to [Manage News Partners on the portal](/../../) feature

# Allow admin user to configure a new partner on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to configure a new integration with partner
    So that user will see the news from a third-party source

## Acceptance criteria

    Scenario: An admin user configures a new integration with partner on the News Partners page
    Given I am logged in as an admin user

    When I view News Partners page with no partners
    Then I see the next elements:
      - Page header in top left corner of the screen
      - +Add New Partner button in the top-right corner of the screen
      - The Empty State message that informs about the absence of integrations with partners, with a link for adding the first one
    When I click on the +Add New Partner button or on the link inside the message
    Then I see the popup with a drop-down list with the available partners is shown
    When I select Google News partner and click Add button 
    Then I see the new element for inactive Google News integration is added to the list on the News partners page
      And I see the form with partner-specific fields is shown:
        - API Key - text field for API Key provided by Google News after the development account activation (mandatory field)
        - Default Sources - text field for comma-separated sources names ( for example "abc-news, associated-press"; mandatory field)
        - Section for news sources configuration for all categories with the next columns:
            - Active - checkbox for configuration activation/deactivation
            - Category - name of the sport category
            - Sources - text field for comma-separated sources names ( "abc-news, associated-press")
          And I see checkbox in Active column title
          When I click on it 
          Then all categories’ checkboxes are selected/deselected
        - Cancel button for changes discarding and closing the form
        - Save button for configuration saving that will be disabled till I make any changes in the form
    When I click cancel button 
    Then I see confirmation popup, where I should confirm that I want to leave the form without saving changes
    When I click on the Confirm button 
    Then I see that form is closed, changes are not saved and integration with this partner stays inactivated
    When I click Save button 
      And I see the fill mandatory fields in (API Key and Default Sources in case of Google News)
      And I see "Configuration is successfully saved" popup in case of success or "Something went wrong, please try again" in case of fail, 
	  both cases have Cross icon on the right top corner 
    When I click on Cross icon or click out of the popup 
    Then I see the the form is closed and I see the list of existing partners 
      And I see that integration with newly added partner is activated
    When mandatory fields are not filled
    Then I see the unfilled fields are highlighted with red and nothing happens with a form

## Mockups

1. Admin user sees News Partners page with no partners
2. Admin user sees “Add New News Partner” popup
3. Admin user sees New News Partner empty form
4. Admin user sees “Something went wrong” popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners page with no partners:**

![Posting in progress](/products/sport_news_portal/web_application_features/manage_news_partners/images/news_partners_page_with_no_partners.png)

**2. Admin user sees “Add New News Partner” popup:**

![Add New News Partner popup](/products/sport_news_portal/web_application_features/manage_news_partners/images/add_new_news_partners_popup.png)

**3. Admin user sees New News Partner empty form:**

![New News Partner empty form](/products/sport_news_portal/web_application_features/manage_news_partners/images/add_new_news_partners_empty_form.png)

**4. Admin user sees “Something went wrong” popup:**

![Something went wrong popup](/products/sport_news_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test Scenarios

1. Verify the content of News Partners page
2. Verify the content of the form with partner-specific fields
3. Verify the cancel button on adding new partner
4. Verify saving new added partner
5. Verify saving new added partner in case of failure
6. Verify clicking on Cross icon or click out of the popup

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of News Partners page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Observe the News Partners page where no partners are added|The next elements should be present:<br> - Page header in top left corner of the screen<br> - +Add New Partner button in the top-right corner of the screen

### **#2. Verify the content of the form with partner-specific fields**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the +Add New Partner button|The empty configuration form will be shown
|5|Select Google News partner from dropdown list -> Click OK|
|6|Observe the form with partner-specific fields|Form with partner-specific fields contains:<br> - API Key<br> - Default Sources<br> - Section for news sources configuration for all categories with the next columns: category, active - switch for configuration activation/deactivation, sources<br> - Switch for the integration activation/deactivation<br> - Cancel button<br> - Save button

### **#3. Verify the cancel button on adding new partner**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the +Add New Partner button|The empty configuration form will be shown
|5|Click Cancel|Confirmation popup to confirm leaving the form without saving changes
|6|Click on the Confirm button|The form is closed and no changes saved

### **#4. Verify saving new added partner**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the +Add New Partner button|The empty configuration form will be shown
|5|Click Save|"Configuration is successfully saved" popup appears
|6|Click on Cross icon|The form will be closed and a new element will be added to the list on the News partners page

### **#5. Verify saving new added partner in case of failure**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the +Add New Partner button|The empty configuration form will be shown
|5|On clicking Save imitate some network disconnection for few seconds|"Something went wrong, please try again" pop up appears

### **#6. Verify clicking on Cross icon or click out of the popup**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the +Add New Partner button|The empty configuration form will be shown
|5|Fill in the mandatory fields|
|6|Click on Save|"Configuration is successfully saved" popup appears
|7|Click on Cross icon or click out of the popup|The form will be closed and I will see the list of existing partners

### **#7. Verify that new partner cannot be saved with empty mandatory fields**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the +Add New Partner button|The empty configuration form will be shown
|5|Fill in the mandatory fields|
|6|Click on Save|Unfilled fields are highlighted with red and nothing happens with a form

</details>

