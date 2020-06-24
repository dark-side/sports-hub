### Back to [Manage teams on the portal](/../../) feature

# Allow admin users to edit the existing Team/Player

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to edit the existing Team/Player
    So that I can change the logo or the name of the existing team

## Acceptance criteria

    Scenario: An admin user double clicks on the team in the list or clicks the Edit link on the record in the list
    Given I am logged in as an admin user

    When I double click on the team record in the list or click the Edit link in the right side of  the record
    Then I see the Edit form next to the map, that consist of the next elements:
      - Select Location drop-down field
      - Select Sports category drop-down field
      - Select Subcategory drop-down field
      - Team/Player field
      - The field with the logo of the team/player
      - Save button that is disabled by default
      - Cancel button
      And I see the form is filled in with values from the selected record
    When I make changes
    Then I see a Save button becomes enabled
    When I change any dropdown field
    Then I see a dropdown fields below become reset
    When I hover the logo
    Then I see the field for uploading the team logo with "Add logo" link
    When I complete the changes and click the Save button
    Then I see "Your team is successfully updated" popup in case of success or "Something went wrong, please try again" in case of fail, both cases are with the Cross icon on the right top corner
    When I click on Cross icon
    Then I see the Edit form with new values and disabled Save button
      And I see the list of the teams filtered by Select fields in the form
    When I click Cancel button
    Then I see the default form for viewing teams/players

## Mockups

1. User sees teams page
2. User sees teams page with active Add Team/Player form
3. User sees Add Team/Player form with no logo
4. User sees Add Team/Player form with logo
5. User sees something went wrong popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees teams page:**

![Teams page Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/teams_page.png)

**2. User sees teams page with active Add Team/Player form:**

![Add Team/Player Active form Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/teams_page_with_active_save_cancel.png)

**3. User sees Add Team/Player form with no logo:**

![Add Team/Player form with no logo Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/add_team_player_no_logo.png)

**4. User sees Add Team/Player form with logo:**

![Add Team/Player form with logo Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/add_team_player_with_logo.png)

**5. User sees something went wrong popup:**

![Something went wrong popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/something_went_wrong_popup.png)

</details>

## Test Scenarios

1. Verify double click on the team record in the list
2. Verify clicking on the Edit link in the right side of the team
3. Verify hovering the logo on the Teams page while editing
4. Verify saving changes in existing team record
5. Verify "Something went wrong, please try again" popup in case of fail

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify double click on the team record in the list**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Double click on the team record in the list|The Edit form next to the map appears, that consist of the next elements:<br>- Select Location drop-down field<br>- Select Sports category drop-down field<br>- Select Subcategory drop-down field<br>- Team/Player field<br>- The field with the logo of the team/player<br>- Save button that is disabled by default<br>- Cancel button

### **#2. Verify clicking on the Edit link in the right side of the team**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Edit link in the right side of the team record|The Edit form next to the map appears, that consist of the next elements:<br>- Select Location drop-down field<br>- Select Sports category drop-down field<br>- Select Subcategory drop-down field<br>- Team/Player field<br>- The field with the logo of the team/player<br>- Save button that is disabled by default<br>- Cancel button

### **#3. Verify hovering the logo on the Teams page while editing**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Edit link in the right side of the team record|The Edit form next to the map appears and the logo is shown
|5|Hover over the logo|The field for uploading the team logo with "Add logo" link appears

### **#4. Verify saving changes in existing team record**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Edit link in the right side of the team record|The Edit form next to the map appears and the logo is shown
|5|Make some changes|Save button becomes enabled
|6|Click on Save button|"Your team is successfully updated" popup appears
|7|Click cross button on the popup|The Edit form with new values is shown and Save button is disabled

### **#5. Verify "Something went wrong, please try again" popup in case of fail**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Edit link in the right side of the team record|The Edit form next to the map appears and the logo is shown
|5|Make some changes|Save button becomes enabled
|6|Click on Save button and try to imitate some network connection lose for few seconds and stabilize it again|"Something went wrong, please try again" popup appears

</details>
