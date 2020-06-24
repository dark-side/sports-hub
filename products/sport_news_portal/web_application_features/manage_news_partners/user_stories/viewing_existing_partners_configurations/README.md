### Back to [Manage News Partners on the portal](../../) feature

# Allow admin users to view an existing partner's configurations on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to view the list of existing partners configurations

## Acceptance criteria

    Scenario: An admin user views the list of existing partners configurations on the News Partners page
    Given I am logged in as an admin user

    When I view News Partners page where at least one partner was added
    Then I see the list with one item per one partner
      And I see that each item has:
       - Plus/Minus icon on the left side for opening/closing the form 
       - Partner's name right after the Plus/Minus icon
       - Switch for the integration activation/deactivation
       - Edit icon
       - Delete icon
    When I click on switch and deactivate integration
    Then I see confirmation popup, where I should confirm that I want to deactivate the partner
    When I click on the Confirm button 
    Then I see that partner is deactivated
    When I click on switch to activate the integration and mandatory fields are filled
    Then I see that partner is activated
    When I click on switch to activate the integration and mandatory fields are not filled
    Then I see the form is opened and required fields are highlighted with red colour

## Mockups

1. Admin user sees News Partners list
2. Admin user sees New News Partner form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![News Partners list](/products/sport_news_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees New News Partner form:**

![New News Partner form](/products/sport_news_portal/web_application_features/manage_news_partners/images/new_news_partners_edit_state.png)

</details>

## Test Scenarios

1. Verify the content of News Partners page
2. Verify clicking on switch switch and deactivate integration
3. Verify clicking on switch to activate the integration and mandatory fields have been filled in 
4. Verify clicking on switch to activate the integration with empty mandatory fields

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of News Partners page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Observe the News Partners page|The next elements should be present:<br> - Plus/Minus icon on the left side for opening/closing the form<br> - Partner's name on the left side<br> - Switch for the integration activation/deactivation<br> - Edit icon<br> - Delete icon

### **#2. Verify clicking on switch switch and deactivate integration**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Observe the News Partners page|
|5|Click on switch and deactivate integration|Confirmation popup appears
|6|Click on the Confirm button|Partner is deactivated

### **#3. Verify clicking on switch to activate the integration and mandatory fields have been filled in **

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Observe the News Partners page|
|5|Click on switch and deactivate integration|
|6|Fill in the fields|Confirmation popup appears
|7|Click on Confirm button|The partner is activated

### **#4. Verify clicking on switch to activate the integration with empty mandatory fields**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Observe the News Partners page|
|5|Click on switch and activate integration|
|6|Leave the fields empty|
|7|Click on confirm button|The form will be opened and required fields will be highlighted with red colour

</details>
