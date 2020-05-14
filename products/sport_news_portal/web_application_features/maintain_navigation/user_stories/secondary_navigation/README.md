### Back to [Maintain Navigation on the portal](/../../) feature

# Allow users to navigate to the team page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to navigate to the team page of the Sport News site using the Navigation menu
    So that I can see news about selected team

## Acceptance criteria

    Scenario: A site user navigates to the team page of the Sport News site using the Navigation menu
    Given I am logged in as a site user

    When I hover over any of the navigation menu subcategory 
    Then I see a mega dropdown menu with the teams available in that subcategory
      (For example if I hover the AFC South subcategory 
      And I see a secondary navigation dropdown is opened with a list of the available teams: Houston, Indianapolis, Jacksonville, Tennessee)
      And I see these teams appear and the order in which they appear in the Content Management System (Information Architecture section)
    When I click on the team
    Then I am taken to the landing page for that team
    When I view a team page of the site 
    Then I see a corresponding navigation menu category item is set to its active state (highlighted)

## Mockups

1. User sees an opened navigation dropdown with teams  


<details>
  <summary>Click here to see mockups details</summary>

**1. User sees an opened navigation dropdown with teams:**

![Navigation dropdown with teams](/products/sport_news_portal/web_application_features/maintain_navigation/images/navigation_dropdown_with_teams.png)

</details>

## Test Scenarios

1. Verify a secondary navigation dropdown of Subcategory
2. Verify clicking  on the Team

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify a secondary navigation dropdown of Subcategory**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Observe main navigation menu|
|4|Hover over the AFC South subcategory|A secondary navigation dropdown is opened
|5|Verify the list of teams in the AFC South subcategory| The list of teams should include:<br> - Houston<br> - Indianapolis<br> - Jacksonville<br> - Tennessee

### **#2. Verify clicking  on the Team**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Observe main navigation menu|
|4|Click on any Team in the subcategory|Admin is navigated to the landing page for chosen team
|5|View a team page of the site|The corresponding navigation menu category item is set to its active state (highlighted)

</details>

