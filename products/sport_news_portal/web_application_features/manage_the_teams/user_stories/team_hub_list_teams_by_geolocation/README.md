### Back to [Manage teams on the portal](/../../) feature

# Allow users to see teams news on Team Hub based on user’s geolocation

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to read news of teams from my geolocation on Team Hub page

## Acceptance criteria

    Scenario: A site user reads news of teams from geolocation on Team Hub page and do not configured favorite teams list and visits Team Hub page
    Given I am logged in as a site user

    When I am on Team Hub page and I did not configure my favorite teams in the personal cabinet
    Then I see a list of news that are sorted per teams that are selected automatically based on my geolocation
      And I see the Most Popular and Most Commentable blocks
      And I see a list of team news contains 3 recent news

## Mockups

1. User sees Team Hub page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Team Hub page:**

![Team Hub page Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/team_hub_page.png)

</details>

## Test Scenarios

1. Verify that the team list on a Team Hub page are selected automatically based on my geolocation
2. Verify that the team list on a Team Hub page could on be selected automatically if geolocation is turn off

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that the team list on a Team Hub page are selected automatically based on my geolocation**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account (with user who did not configure favorite teams list and has geolocation is turn on)|
|3|Click on Team Hub item in the left side bar|
|4|Observe the team list|The system displays a list of news that are sorted per teams that are selected automatically based on my geolocation

### **#2. Verify that the team list on a Team Hub page could on be selected automatically if geolocation is turn off**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account (with user who did not configure favorite teams list and has geolocation is turn off)|
|3|Click on Team Hub item in the left side bar|
|4|Observe the team list|The list of news is empty

</details>
