### Back to [Manage teams on the portal](../../) feature

# Allow users to see Team Hub management page in the personal cabinet

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to have a Team Hub management page
    So that I can customize the news

## Acceptance criteria

    Scenario: A site user visits Team Hub management page
    Given I am logged in as a site user

    When I view any page of the application
      And I click on the drop-down menu next to my avatar at the top of the page
    Then I  see a link to Team Hub page
    When I click on Team Hub
    Then I see that system takes me to my profile page
      And I see the Team Hub tab is active
      And I see the list with my favorite teams and a link to "Manage Teams List"

## Mockups

1. User sees Team Hub management page
2. User sees Team Hub management page with hovered team

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Team Hub management page:**

![Team Hub management page Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_team_hub_page.png)

**2. User sees Team Hub management page with hovered team:**

![Team Hub management page with hovered team Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_team_hub_page_delete_team.png)

</details>

## Test Scenarios

1. Verify the content of the Team Hub tab on the profile page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify Manage Teams List button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user’s avatar at the top of the page|
|4|Click on Team Hub|
|5|Check the content of the Team Hub tab|The Team Hub contains a list with user’s favorite teams "Manage team list" button

</details>
