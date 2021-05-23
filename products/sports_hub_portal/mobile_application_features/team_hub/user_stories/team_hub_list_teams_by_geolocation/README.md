### Back to [Team hub: news about favorite teams](../../) feature

# Allow users to see teams news on Team hub based on their geolocation

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to be able to read news of teams based on my geolocation on the Team Hub page in case of no teams are followed

## Acceptance criteria

<pre>
<b><i>Scenario: A logged-in users reads news about teams from their geolocation on the Team hub page</i></b>

Given I am logged in as an user

When I am on the <b>Team Hub</b> page and I haven’t configured my favorite teams in the <b>Team Hub</b> configuration page
Then I see a list of news that are sorted according to the teams that are selected automatically based on my geolocation
  And I see the <b>Most popular</b> and <b>Most commented</b> sections
  And I see a list of each team news contains 3 recent news
</pre>

## Mockups

1. Users see <b>Team hub</b> in the navigation menu
2. Users see news on the <b>Team hub</b> page
3. Full <b>Team hub</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Team hub in the navigation menu:**

![Users see Team hub in the navigation menu](/products/sports_hub_portal/mobile_application_features/team_hub/images/application_navigation_menu.png)

**2. Users see news on the Team hub page:**

![Users see news on the Team hub page](/products/sports_hub_portal/mobile_application_features/team_hub/images/application_team_hub_page.png)

**3. Full Team hub page:**

![Full Team hub page](/products/sports_hub_portal/mobile_application_features/team_hub/images/team_hub_full_page.png)

</details>

## Test cases

1. Verify that the team list on the <b>Team Hub</b> page is selected automatically based on my geolocation
2. Verify that the team list on the <b>Team Hub</b> page could not be selected automatically if geolocation is turned off

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the team list on the Team Hub page is selected automatically based on my geolocation**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user did not configure the Favorite teams list and visits the <b>Team Hub</b> page</br>- Geolocation is turned on</br>- The user is logged in</br>- The user is on the <b>Team Hub</b> page|1) Examine the teams list|1) The list of news is shown and sorted according to the teams that are selected automatically based on my geolocation|

### **#2. Verify that the team list on the Team Hub page could not be selected automatically if geolocation is turned off**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user did not configure the favorite teams list and visits the <b>Team Hub</b> page</br>- Geolocation is turned off</br>- The user is logged in</br>- The user is on <b>Team Hub</b> page|1) Examine the teams list|1) The list of news is empty|

</details>
