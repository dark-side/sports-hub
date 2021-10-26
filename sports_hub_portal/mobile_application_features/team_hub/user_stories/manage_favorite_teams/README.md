### Back to [Team hub: news about favorite teams](../../) feature

# Allow users to view videos in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to select my favorite teams

## Acceptance criteria

<pre>
<b><i>Scenario: A logged-in user selects favorite teams</i></b>

Given I am logged in as a user

When I view any page of the application
And I tap my profile picture at the top of the page
Then I see the <b>Team hub</b> menu item

When I tap <b>Team hub</b>
Then I see the <b>Team hub</b> configuration page is opened

When I view the <b>Team Hub</b> configuration page
Then I see the following:
  - "Team Hub" header
  - Search icon
  - The list with my favorite teams with the <b>Delete</b> icons
  - The <b>Manage Teams List</b> button

When I tap <b>Manage Teams List</b>
Then I see the search field that has the "Type a team name" placeholder
  And I see a list of already selected teams with the Delete icon on the right

When I enter any letter into the search field
Then I see the list of teams changes according to the entered letters

When I select a team from the list and click <b>Follow</b>
Then I see the list with the selected team in it and the <b>Manage Teams List</b> button

When I tap <b>Manage Teams List</b>
  And I tap the Delete icon on the right of any team
Then the team is removed from the list
  And I see the list without the removed team
</pre>

## Mockups

1. Users see <b>Team hub</b> in the profile menu
2. Users see a list of followed teams on the <b>Team hub</b> configuration page
3. Users see the <b>Team hub</b> configuration page
4. Users see suggestions according to the entered team name

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Team hub in the profile menu:**

![Users see Team hub in the profile menu](/sports_hub_portal/mobile_application_features/team_hub/images/application_profile_menu.png)

**2. Users see a list of followed teams on the <b>Team hub</b> configuration page:**

![Users see a list of followed teams on the <b>Team hub</b> configuration page](/sports_hub_portal/mobile_application_features/team_hub/images/application_followed_teams_team_hub_configuration_page.png)

**3. Users see the Team hub configuration page:**

![Users see the Team hub configuration page](/sports_hub_portal/mobile_application_features/team_hub/images/application_team_hub_configuration_page.png)

**4. Users see suggestions according to the entered team name:**

![Users see suggestions according to the entered team name](/sports_hub_portal/mobile_application_features/team_hub/images/application_team_hub_configuration_page_team_search.png)

</details>

## Test cases

1. Verify the content of the <b>Team Hub</b> configuration page
2. Verify the <b>Manage Teams List</b> button
3. Verify searching teams in the placeholder "Type a team name"
4. Verify selecting a team to follow
5. Verify deleting team from the list of teams to follow

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Team Hub configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header tap the profile picture</br>2) Tap the <b>Team Hub</b> item</br>3) Check the content of the <b>Team Hub</b> configuration page|3) The Team Hub configuration page contains following:</br>- "Team Hub" header</br>- Search icon</br>- The list with my favorite teams with the <b>Delete</b> icons</br>- The <b>Manage Teams List</b> button|

### **#2. Verify the Manage Teams List button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header tap the profile picture</br>2) Tap the <b>Team Hub</b> item</br>3) Tap <b>Manage Team List</b>|3) A search field appears that has the "Type a team name" placeholder and the list of already selected teams with the delete icons to remove them is shown|

### **#3. Verify searching teams in the placeholder "Type a team name"**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header tap the profile picture</br>2) Tap the <b>Team Hub</b> item</br>3) Tap <b>Manage Team List</b></br>4) Type any letter into the search field|2) The <b>Team Hub page</b> contains a list with user’s favorite teams and the <b>Manage Team List</b> button</br>3) A search field appears that has the "Type a team name" placeholder and the list of already selected teams with the delete icons to remove them is shown</br>4) The list of teams that satisfies the search is shown|

### **#4. Verify selecting a team to follow**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header tap the profile picture</br>2) Tap the <b>Team Hub</b> item</br>3) Tap <b>Manage Team List</b></br>4) Type any letter into the search field</br>5) Select a team from the list and click <b>Follow</b>|5) Selected team appears in the list of teams|

### **#5. Verify deleting team from the list of teams to follow**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) In the page header tap the profile picture</br>2) Tap the <b>Team Hub</b> item</br>3) Tap <b>Manage Team List</b></br>4) Next to any team, tap the <b>Delete</b> icon|4) The team is removed from the list of followed teams|
</details>
