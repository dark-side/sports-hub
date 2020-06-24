### Back to [Manage teams on the portal](../../) feature

# Allow admin users to add a new Team/Player

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to add a new Team/Player

## Acceptance criteria

    Scenario: An admin user clicks on +Add Team/Player button
    Given I am logged in as an admin user

    When I click on +Add Team/Player button
    Then I see a new form next to the map, that consists of the next elements:
      - Select Location drop-down field
      - Select Sports category drop-down field
      - Select Subcategory drop-down field
      - Team/Player field
      - The field for uploading the team logo with "Add logo" link
      - Add to list button
      - Cancel button
    When I added a logo and hover on it
    Then I see the field for uploading the team logo with "Add logo" link
    When I complete the form and click the Add to List button
    Then I see "Your team is successfully added" popup in case of success or "Something went wrong, please try again" in case of fail, both cases are with the Cross icon on the right top corner
    When I click on Cross icon
    Then I see the list of the teams filtered by Select fields in the form
      And I see that a new team is added to the top of the list
      And I see Edit Team/Player button instead of the Add to List button
    When I click Cancel button
    Then I see the default form for viewing teams

## Mockups

1. User sees teams page
2. User sees teams page with active Add Team/Player form
3. User sees Add Team/Player form with no logo
4. User sees Add Team/Player form with logo
5. User sees Team is added popup
6. User sees something went wrong popup

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

**5. User sees Team is added popup:**

![Team is added Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/team_added_popup.png)

**6. User sees something went wrong popup:**

![Something went wrong popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/something_went_wrong_popup.png)

</details>

## Test Scenarios

1. Verify +Add Team/Player button on the Teams page
2. Verify that a new team is added to the top of the list
3. Verify Cancel button on the Teams page
4. Verify "Something went wrong, please try again" pop-up

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify +Add Team/Player button on the Teams page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on +Add Team/Player button|A new form next to the map appears, that consists of the next elements<br>- Select Location drop-down field<br>- Select Sports category drop-down field<br>- Select Subcategory drop-down field<br>- Team/Player field<br>- The field for uploading the team logo with "Add logo" link<br>- Add to list button<br>- Cancel button
|5|Complete the form and click the Add to List button|"Your team is successfully added" popup in case of success

### **#2. Verify that a new team is added to the top of the list**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on +Add Team/Player button|
|5|Complete the form and click the Add to List button|"Your team is successfully added" popup in case of success
|6|Click on Cross button of the "Your team is successfully added" popup|A new team is added to the top of the list filtered by Select fields

### **#3. Verify Cancel button on the Teams page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on +Add Team/Player button|A new form next to the map appears
|5|Complete the form and click the Cancel button|The default form for viewing teams is shown

### **#4. Verify "Something went wrong, please try again" pop-up**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on +Add Team/Player button|A new form next to the map appears, that consists of the next elements<br>- Select Location drop-down field<br>- Select Sports category drop-down field<br>- Select Subcategory drop-down field<br>- Team/Player field<br>- The field for uploading the team logo with "Add logo" link<br>- Add to list button<br>- Cancel button
|5|Complete the form|
|6|Imitate some network disconnection and stabilize it again|
|7|Click the Add to List button|"Something went wrong, please try again" popup in case of fail

</details>
