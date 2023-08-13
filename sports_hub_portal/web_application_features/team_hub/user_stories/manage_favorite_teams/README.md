### Back to [Team hub: news about favorite teams](../../README.md) feature

# Allow users to manage favorite teams in the personal cabinet

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to select my favorite teams

## Acceptance criteria

<pre>
<b><i>Scenario: A logged-in user selects favorite teams</i></b>

Given I am logged in to the portal

When I view any page of the application
  And I click the drop-down menu next to my profile picture at the top of the page
Then I see a link to <b>Team hub</b> page

When I click <b>Team hub</b>
Then I am taken to <b>Team hub</b> configuration page in my cabinet

And I click <b>Manage teams list</b>
Then I see the search input with the <b>Follow</b> button
  And I see a list of already selected teams

When I enter any letter into the search box
Then I see the matching list of the teams' names

When I select a team from the list and click <b>Follow</b>
Then I see the selected team is added to the list

When I click <b>Manage teams list</b>
  And hover over any team
Then I see a delete icon

When I click the delete icon
Then the team is removed from the list
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a link to the <b>Team hub</b> management page
2. Users see the <b>Team hub</b> management page
3. Users see the page after clicking <b>Manage teams list</b>
4. Users see the search team results
5. Users see the search field after selecting the team

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a link to the Team hub management page:**

![Users see a link to the Team hub management page](/sports_hub_portal/web_application_features/team_hub/images/link_to_my_teams_page.png)

**2. Users see the Team hub management page:**

![Users see the Team hub management page](/sports_hub_portal/web_application_features/team_hub/images/my_teams_management_page.png)

**3. Users see the page after clicking Manage teams list:**

![Users see the page after clicking Manage teams list](/sports_hub_portal/web_application_features/team_hub/images/manage_my_teams_form.png)

**4. Users see the search team results:**

![Users see the search team results](/sports_hub_portal/web_application_features/team_hub/images/search_team_result.png)

**5. Users see the search field after selecting the team:**

![Users see the search field after selecting the team](/sports_hub_portal/web_application_features/team_hub/images/search_team_selected_team.png)

</details>

## Test cases

1. Verify the content of the Team hub tab on the profile page
2. Verify the <b>Manage teams list</b> button
3. Verify that the search field proposes teams according to the entered text
4. Verify selecting a team to follow
5. Verify deleting a team from the list

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Team hub tab on the profile page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header next to the user’s profile picture click the drop-down button</br>2) Select <b>Team hub</b> from the drop-down menu</br>3) Check the content of the <b>Team hub</b> tab|4) The <b>Team hub</b> tab contains a list with user’s favorite teams and the <b>Manage team list</b> button|

### **#2. Verify the Manage teams list button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header next to the user’s profile picture click the drop-down button</br>2) Select <b>Team hub</b> from the drop-down menu</br>3) Click <b>Manage team list</b> link at the bottom of the list|3) The search field with "Type a team name" placeholder and delete icon on hover for existing teams appear|

### **#3. Verify that the search field proposes teams according to the entered text**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some teams to be added which contain "Los"|1) In the page header, next to the user’s profile picture click the drop-down button</br>2) From the drop-down menu, select <b>Team hub</b></br>3) Click <b>Manage team list</b></br>4) Type "Los" into the search field|4) There are only teams that contain "Los" are included in the list|

### **#4. Verify selecting a team to follow**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- Go to <b>Team hub</b>|1) Click <b>Manage team list</b></br>2) Select some team from the list and click <b>Follow</b>|2) Selected team appears on the list. Users can see news about selected team on the <b>Team hub</b> page|

### **#5. Verify deleting a team from the list**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- Go to <b>Team hub</b></br>- There are some teams followed by the user|1) Click <b>Manage team list</b></br>2) Click <b>Delete</b> any team|2) The team is removed from the list. The user does not see news about the selected team on the <b>Team hub</b> page|
</details>
