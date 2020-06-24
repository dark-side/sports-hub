### Back to [Manage News Partners on the portal](../../) feature

# Allow admin users to edit the existing partner's configurations on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to change the existing partner's configurations

## Acceptance criteria

    Scenario: An admin user changes the existing partner's configurations on the News Partners page
    Given I am logged in as an admin user

    When I click the Edit icon or the Plus icon for the needed partner on the News Partners page
    Then I see edit form with pre populated partners configurations below the row for this partner in the partners' list on the News Partner page
      And I see the edit form consists of the partner-specific fields (example for Google News):
        - API Key - text field for API Key provided by Google News after the development account activation 
        - Default Sources - text field for comma-separated sources names (for example "abc-news, associated-press")
        - Section for news sources configuration for all categories with the next columns:
            - Active - checkbox for configuration activation/deactivation
            - Category - name of the sport category
            - Sources - text field for comma-separated sources names ( "abc-news, associated-press")
        - Cancel button for changes discarding  and closing the form
        - Save button for configuration saving that will be disabled till I make any changes in the form
    When I click Cancel button 
    Then I see confirmation popup, where I should confirm that I want to leave the form without saving changes
    When I click on the Confirm button
    Then I see that form is closed and no changes were saved
    When I click Save button 
    Then I see "Configuration is successfully saved" popup in case of success or "Something went wrong, please try again" in case of fail, both cases have Cross icon on the right top corner 
    When I click on Cross icon
    Then I see the form is closed
    And I see the list of existing partners

## Mockups

1. Admin user sees News Partners list
2. Admin user sees New News Partner form
3. Admin user sees “Something went wrong” popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![News Partners list](/products/sport_news_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees New News Partner form:**

![New News Partner form](/products/sport_news_portal/web_application_features/manage_news_partners/images/new_news_partners_edit_state.png)

**3. Admin user sees “Something went wrong” popup:**

![Something went wrong popup](/products/sport_news_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test Scenarios

1. Verify the content of News Partners page
2. Verify the content of News Partners page
3. Verify the cancel button on adding new partner
4. Verify saving changes after editing news partner
5. Verify saving changes after editing news partner in case of failure

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of News Partners page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Click on Edit link|The Edit form with pre populated partners configurations appears below the row for this partner in the partners' list on the News Partner page

### **#2. Verify the content of News Partners page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Click on Edit link|The Edit form with pre populated partners configurations appears below the row for this partner in the partners' list on the News Partner page
|5|Observe the Edit form|The Edit form should contain such elements:<br> - API Key<br> - Default Sources<br> - Section for news sources configuration for all categories with the next columns: category, active, sources<br> - Current Switch has been removed for both new and edit cases<br> - Cancel button<br> - Save button

### **#3. Verify the cancel button on adding new partner**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the Edit button|The Edit form with pre populated partners configurations appears
|5|Make some changes|
|6|Click Cancel|Confirmation popup to confirm leaving the form without saving changes
|7|Click on the Confirm button|The form is closed and no changes saved

### **#4. Verify saving changes after editing news partner**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the Edit button|The Edit form with pre populated partners configurations appears
|5|Make some changes|
|6|Click Save|"Configuration is successfully saved" popup appears
|7|Click on Cross icon|The form will be closed and a new element will be added to the list on the News partners page

### **#5. Verify saving changes after editing news partner in case of failure**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|The admin is navigating to News Partner Page
|4|Click on the Edit button|The Edit form with pre populated partners configurations appears
|5|Make some changes|
|6|On clicking Save imitate some network disconnection for few seconds|"Something went wrong, please try again" pop up appears

</details>
