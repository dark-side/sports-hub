### Back to [Manage Pages on the portal](../../) feature

# Allow admin user to view a list of categories on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to view a list of site categories (site navigation menu items) 
    So that I can navigate to configuration page for the selected menu item (category)

## Acceptance criteria

    Scenario: An admin user views a list of site categories (site navigation menu items)
    Given I am logged in as an admin user

    When I view any page in the CMS
    Then I see a horizontal navigation under the site header with a list of categories (menu items)
    When I click on any of the horizontal navigation item (aka category)
    Then I am taken to the category configuration page
      And I see that selected category name is displayed in the section under the site header and above the horizontal navigation
      And I see that selected category name is displayed at the left side of that section 
      And I see that Save changes button is displayed at the right side of that section 
    For example when I click on the Home category
    Then I’m taken to the Home category configuration page

## Mockups

1. Admin user sees horizontal navigation under the site header with a list of menu items

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees horizontal navigation under the site header with a list of menu items:**

![Horizontal navigation under the site header](/products/sport_news_portal/web_application_features/manage_pages/images/cms_horizontal_navigation.png)

</details>

## Test Scenarios

1. Verify horizontal navigation under the site header on every CMS page
2. Verify clicking on the horizontal navigation item
3. Verify that category name is displayed in the section under the site header
4. Verify Save button on CMS page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify horizontal navigation under the site header on every CMS page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on the Surveys/Banners/Social networks etc in the left Sidebar menu|
|4|Observe the horizontal navigation|Horizontal navigation is present under the site header with a list of categories on every CMS page

### **#2. Verify clicking on the horizontal navigation item**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site
|2|Log in your admin account
|3|Click on any of the horizontal navigation ite|Admin is taken to the category configuration page

### **#3. Verify that category name is displayed in the section under the site header**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on any of the horizontal navigation item|Admin is taken to the category configuration page
|4|Check the category name on the page|Category name is displayed in the section under the site header

### **#4. Verify Save button on CMS page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on Home category|Admin is taken to the category configuration page
|4|Check if save button is present on a page|Save changes button is displayed at the right side of that section

</details>
