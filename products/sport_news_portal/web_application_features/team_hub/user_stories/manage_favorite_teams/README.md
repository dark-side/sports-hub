### Back to [Team hub - news of favorite teams](../../) feature

# Allow users to manage favorite teams in the personal cabinet

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to select my favorite teams

## Acceptance criteria

<pre>
Scenario: A logged-in user selects favorite teams
Given I am logged in to the portal

When I view any page of the application
  And I click on the drop-down menu next to my profile picture at the top of the page
Then I see a link to <b>My teams</b> page

When I click <b>My teams</b>
Then I am taken to <b>My teams</b> configuration page in my cabinet

And I click <b>Manage teams list</b>
Then I see the search input with <b>Follow</b> button
  And I see a list of already selected teams

When I enter any letter into the search box
Then I see the matching list of the teams' names

When I select a team from the list and click <b>Follow</b>
Then I see the selected team is added into the list

When I click <b>Manage teams list</b>
  And hover over any team
Then I see a delete icon

When I click on the delete icon
Then the team is removed from the list
</pre>

## Mockups

1. User sees a link to My teams management page
2. User sees a My teams management page
3. User sees the page after clicking the Manage teams list
4. User sees the search team results
5. User sees the search field after selecting the team

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a link to My teams management page:**

![User sees a link to My teams management page](/products/sport_news_portal/web_application_features/team_hub/images/link_to_my_teams_page.png)

**2. User sees a My teams management page:**

![User sees a My teams management page](/products/sport_news_portal/web_application_features/team_hub/images/my_teams_management_page.png)

**3. User sees the page after clicking the Manage teams list:**

![User sees the page after clicking the Manage teams list](/products/sport_news_portal/web_application_features/team_hub/images/manage_my_teams_form.png)

**4. User sees the search team results:**

![User sees the search team results](/products/sport_news_portal/web_application_features/team_hub/images/search_team_result.png)

**5. User sees the search field after selecting the team:**

![User sees the search field after selecting the team](/products/sport_news_portal/web_application_features/team_hub/images/search_team_selected_team.png)

</details>

## Test cases

1. Verify the content of the Team hub tab on the profile page
2. Verify Manage teams list button
3. Verify the search field proposes teams according to the entered text
4. Verify selecting a team to follow
5. Verify deleting team from the list

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Team hub tab on the profile page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account|1) In the page header next to the user’s profile picture click the drop-down button</br>2) Select <b>My teams</b> from the drop-down menu</br>3) Check the content of the <b>Team hub</b> tab|4) The <b>Team hub</b> tab contains a list with user’s favorite teams and the <b>Manage team list</b> button|

### **#2. Verify Manage teams list button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account|1) In the page header next to the user’s profile picture click the drop-down button</br>2) Select <b>My teams</b> from the drop-down menu</br>3) Click <b>Manage team list</b> link at the bottom of the list|3) The search field with "Type a team name" placeholder and delete icon on hover for existing teams appear|

### **#3. Verify the search field proposes teams according to the entered text**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There are some teams to be added which contain "Los"|1) In the page header, next to the user’s profile picture click the drop-down button</br>2) From the drop-down menu, select <b>My teams</b></br>3) Click <b>Manage team list</b></br>4) Type "Los" into the search field|4) There are only teams that contain "Los" suggested in the list|

### **#4. Verify selecting a team to follow**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- Go to <b>My teams</b>|1) Click <b>Manage team list</b></br>2) Select some team from the list and click <b>Follow</b>|2) Selected team appears on the list. User can see news about selected team on the <b>Team hub</b> page|

### **#5. Verify deleting team from the list**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- Go to <b>My teams</b></br>- There are some teams followed by the user|1) Click <b>Manage team list</b></br>2) Click <b>Delete</b> any team|2) The team is removed from the list. User does not see news about selected team on the <b>Team hub</b> page|
</details>