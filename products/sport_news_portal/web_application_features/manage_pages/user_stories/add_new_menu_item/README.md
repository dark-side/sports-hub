### Back to [Manage Pages on the portal](../../) feature

# Allow admin user to add a new menu item for a portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to add a new menu item for a Sport News site

## Acceptance criteria

    Scenario: An admin user adds a new menu item for a Sport News site
    Given I am logged in as an admin user

    When I view any page in the CMS
    Then I see a Add Menu Item button in the Header section
    When I click on this button
    Then I see a dialog window is opened with a input for a menu item name and two buttons Cancel and Add
    When I fill in the name and click on the Add button
    Then I see a new menu item is created 
      And I see this new menu item is displayed in the Site Navigation Menu and in the horizontal navigation in the CMS

## Mockups

1. Admin user sees horizontal navigation under the site header with a list of menu items
2. Admin user sees "Add new menu item" popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees horizontal navigation under the site header with a list of menu items:**

![Horizontal navigation under the site header](/products/sport_news_portal/web_application_features/manage_pages/images/cms_horizontal_navigation.png)

**2. Admin user sees "Add new menu item" popup:**

!["Add new menu item" popup](/products/sport_news_portal/web_application_features/manage_pages/images/add_new_menu_item_popup.png)

</details>

## Test Scenarios

1. Verify Add Menu Item button on horizontal navigation
2. Verify that admin is able to create page for a Sport News site

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify Add Menu Item button on horizontal navigation**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on any category on horizontal navigation|Admin is taken to the category configuration page
|4|Check the presence of Add Menu item button|Add Menu Item button is present in the Header section

### **#2. Verify that admin is able to create page for a Sport News site**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on any category on horizontal navigation|Admin is taken to the category configuration page
|4|Click on Add Menu item button|The dialog window is opened with a input for a menu item name and two buttons Cancel and Add
|5|Fill in the name click on the Add button|This new menu item is displayed in the Site Navigation Menu and in the horizontal navigation in the CMS

</details>
