### Back to [Manage teams on the portal](../../) feature

# Allow users to see Team Hub page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to go to Team Hub page
    So that I can read news of my favorite teams

## Acceptance criteria

    Scenario: A site user visits the Team Hub page
    Given I am logged in as a site user

    When I am on any page of the application
    Then I see the Team Hub page menu item in the left sidebar
    When I click on Team Hub
    Then I see a list of news that are sorted per teams I selected in my personal cabinet
      And I see the Most Popular and Most Commentable blocks
      And I see a list of team news contains 3 recent news and Unfollow button
    When I click on the Unfollow button
    Then I see a confirmation popup
    When I click continue
    Then I see the team news disappears from the page
      And I see a notification message "You have unfollowed the team {team name}!"

## Mockups

1. User sees Team Hub page
2. User sees Team Hub page with a single followed team
3. User sees Unfollow team confirmation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Team Hub page:**

![Team Hub page Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/team_hub_page.png)

**2. User sees Team Hub page with a single followed team:**

![Team Hub page with a single followed team Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/team_hub_single_followed_team_page.png)

**3. User sees Unfollow team confirmation popup:**

![Unfollow team confirmation popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/unfollow_team_confirmation_popup.png)

</details>

## Test Scenarios

1. Verify clicking on unfollow button
2. Verify canceling unfollow process

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify clicking on unfollow button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on Team Hub item in the left side bar|The system displays a list of news that are sorted per teams and each list of team news contains 3 recent news and Unfollow button
|4|Click on the Unfollow button|The system displays a confirmation popup
|5|Click to continue on the confirmation popup|The team news disappears from the page and the system displays a notification message "You have unfollowed the team {team name}!"

### **#2. Verify canceling unfollow process**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Click on Team Hub item in the left side bar|The system displays a list of news that are sorted per teams and each list of team news contains 3 recent news and Unfollow button
|4|Click on the Unfollow button|The system displays a confirmation popup
|5|Click one cancel on the confirmation popup|The team news are still following by the user

</details>
