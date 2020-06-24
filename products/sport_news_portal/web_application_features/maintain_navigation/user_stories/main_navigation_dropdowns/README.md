### Back to [Maintain Navigation on the portal](../../) feature

# Allow users to navigate to the sport subcategory page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to navigate to the sport subcategory page of the Sport News site using the Navigation menu
    So that I can see news about selected subcategory

## Acceptance criteria

    Scenario: A site user navigates to the sport subcategory page of the Sport News site using the Navigation menu
    Given I am logged in as a site user

    When I hover over any of the navigation menu item (category)
    Then I see a mega dropdown menu with the subcategories available in that category
      (For example if I hover the NFL sport category
      And I see a navigation dropdown is opened with a list of the following subcategories: AFC East, AFC North, AFC South, AFC West, NFC East, NFC North, NFC South, NFC West)
      And I see these subcategories appear and the order in which they appear in the Content Management System (Information Architecture section)
    When I click on the navigation menu subcategory item
    Then I am taken to the landing page for that subcategory
    When I view a page within a subcategory of the site 
    Then I see a corresponding navigation menu category item is set to its active state (highlighted)

## Mockups

1. User sees an opened navigation dropdown with subcategories 

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees an opened navigation dropdown with subcategories:**

![Navigation dropdown with subcategories](/products/sport_news_portal/web_application_features/maintain_navigation/images/navigation_dropdown_with_subcategories.png)

</details>

## Test Scenarios

1. Verify navigation menu mega dropdown of Category
2. Verify clicking on the navigation menu subcategory item

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify navigation menu mega dropdown of Category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Observe main navigation menu|
|4|Hover over the NFL sport category|Navigation menu mega dropdown is opened
|5|Verify the list of subcategories in the NFL sport category|The following subcategories are in the of NFL sport category:<br> - AFC East<br> - AFC North<br> - AFC South<br> - AFC West<br> - NFC East<br> - NFC North<br> - NFC South<br> - NFC West

### **#2. Verify clicking on the navigation menu subcategory item**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site
|2|Log in the admin account|
|3|Observe main navigation menu|
|4|Сlick on any navigation menu subcategory item|Admin is navigating to the landing page for that subcategory
|5|View a page within a subcategory of the site|The corresponding navigation menu category item is set to its active state (highlighted)

</details>

