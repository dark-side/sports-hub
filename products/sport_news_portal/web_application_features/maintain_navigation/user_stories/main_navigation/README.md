### Back to [Maintain Navigation on the portal](/../../) feature

# Allow users to view the navigation menu on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to views the Navigation menu on every page of the Sport News site
    So that I can navigate between sport categories pages

## Acceptance criteria

    Scenario: A site user views the Navigation menu on every page of the Sport News site
    Given I am logged in as a site user

    When I view any page on the site 
    Then I see the main navigation menu in the left side bar with the following categories: 
    HOME, NFL, NBA, MLB, NHL, CBB, CFB, NASCAR, GOLF, SOCCER, LIFESTYLE, DEALBOOK, VIDEO, TEAM HUB, Follow on social block (Facebook, Twitter, Google +, Youtube)
      And I see these categories appear and the order in which they appear in the Content Management System (Information Architecture section)
    When I click on a navigation menu category
    Then I am taken to the landing page for that sport category 
    When I view any category page of the site 
    Then I see the corresponding navigation menu category item is set to its active state (highlighted)

## Mockups

1. User sees the main navigation menu in the left side of the page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees the main navigation menu in the left side of the page:**

![Main navigation menu](/products/sport_news_portal/web_application_features/maintain_navigation/images/main_navigation.png)

</details>

## Test Scenarios

1. Verify content of main navigation menu
2. Verify clicking on a navigation menu category

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify content of main navigation menu**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Observe main navigation menu|The main navigation menu is situated in the left side bar
|4|Observe the list of categories|The following categories should be present:<br> - NFL<br> - NBA<br> - MLB<br> - NLH<br> - CBB<br> - CFB<br> - NASCAR<br> - GOLF<br> - SOCCER<br> - MORE<br> - LIFESTYLE<br> - DEALBOOK<br> - VIDEO<br> - Follow on social block (Facebook, Twitter, Google +, Youtube)

### **#2. Verify clicking on a navigation menu category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Сlick on a navigation menu category|Admin is navigating to the landing page for that sport category
|4|View sport category|The corresponding navigation menu category item is set to its active state (highlighted)

</details>
