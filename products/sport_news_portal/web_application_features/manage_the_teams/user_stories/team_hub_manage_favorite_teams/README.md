### Back to [Manage teams on the portal](../../) feature

# Allow users to manage favorite teams in the personal cabinet

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to select my favorite teams

## Acceptance criteria

    Scenario: A site user visits The Team Hub management page and selects my favorite team
    Given I am logged in as a site user

    When I am on Team Hub page in the personal cabinet
      And I click on Manage Teams List
    Then I see a search that has a placeholder "Type a team name"
      And I see a list of my already selected teams with a delete icon in front of them
    When I type any letter
    Then I see a list of teams that satisfy the search
    When I select a team from the list and click Follow
      And I see a list with the selected team in it and a link to "Manage Teams List"
    When I click on Select Your Teams
      And I click on a delete icon in front of any team
      And the team is removed from the list when I click delete icon
    Then I see a list without the removed team

## Mockups

1. User sees Team Hub management page
2. User sees Team Hub management page with hovered team
3. User sees Team Hub management page -> Team search
4. User sees Team Hub management page -> Team is found

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Team Hub management page with hovered team:**

![Team Hub management page Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_team_hub_page.png)

**2. User sees Team Hub management page with hovered team:**

![Team Hub management page with hovered team Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_team_hub_page_delete_team.png)

**3. User sees Team Hub management page -> Team search:**

![Team search Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_team_hub_page_follow_team.png)

**4. User sees Team Hub management page -> Team is found:**

![Team is found Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_team_hub_page_follow_team_search.png)

</details>

## Test Scenarios

1. Verify Manage Teams List button
2. Verify a placeholder "Type a team name"
3. Verify selecting team to follow
4. Verify deleting team from the selecting list of teams to follow

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify Manage Teams List button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user’s avatar at the top of the page|
|4|Click on "Team Hub" link button|The Team Hub page contains a list with user’s favorite teams and "Manage team list" button
|5|Click on Manage Team List button|The system displays a search that has a "Type a team name" placeholder and a list of my already selected teams with a delete icon in front of them

### **#2. Verify a placeholder "Type a team name"**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user’s avatar at the top of the page|
|4|Click on "Team Hub" link button|The Team Hub page contains a list with user’s favorite teams and "Manage team list" button
|5|Click on Manage Team List button|The system displays a search that has a "Type a team name" placeholder and a list of my already selected teams with a delete icon in front of them
|6|Type any letter in the "Type a team name" placeholder|Then the system displays a list of teams that satisfy the search

### **#3. Verify selecting team to follow**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user’s avatar at the top of the page|
|4|Click on "Team Hub" link button|The Team Hub page contains a list with user’s favorite teams and "Manage team list" button
|5|Click on Manage Team List button|The system displays a search that has a "Type a team name" placeholder and a list of my already selected teams with a delete icon in front of them
|6|Select a team from the list and click Follow|The system displays a list with the selected team in it

### **#4. Verify deleting team from the selecting list of teams to follow**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on a drop-down menu next to the user’s avatar at the top of the page|
|4|Click on "Team Hub" link button|The Team Hub page contains a list with user’s favorite teams and "Manage team list" button
|5|Click on Manage Team List button|The system displays a search that has a "Type a team name" placeholder and a list of my already selected teams with a delete icon in front of them
|6|Click on the delete icon in front of any team|The team is removed from the list when I click delete icon and the system displays a list without the removed team

</details>
