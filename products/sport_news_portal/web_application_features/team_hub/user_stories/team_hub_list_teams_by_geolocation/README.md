### Back to [Team hub - news of favorite teams](../../) feature

# Allow users to see teams news on Team Hub based on user’s geolocation

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to read news of teams from my geolocation on the Team hub page when I haven’t configured favorite teams

## Acceptance criteria

<pre>
Scenario: A logged-in user reads news of teams from his geolocation on the Team hub page
Given I am logged in as a site user

When I am on the <b>Team hub</b> page and I haven’t configured my favorite teams in the personal cabinet
Then I see a list of news that are sorted according to the teams that are selected automatically based on my geolocation
</pre>

## Mockups

1. User sees Team Hub page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Team Hub page:**

![User sees Team Hub page](/products/sport_news_portal/web_application_features/team_hub/images/team_hub_geolocation_teams.png)

</details>

## Test cases

1. Verify that the team list on the Team hub page is selected automatically based on my geolocation
2. Verify that the team list on the Team hub page is empty if geolocation is turned off

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the team list on the Team hub page is selected automatically based on my geolocation**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There are no teams followed by the user</br>- Geolocation is turned on|1) On the left sidebar menu, select <b>Team hub</b></br>2) Examine the team list|2) There are news for each team that belongs to the user’s geolocation. There are the <b>Most Popular</b> and <b>Most Commented</b> sections in case they are enabled by admin|

### **#2. Verify that the team list on the Team hub page is empty if geolocation is turned off**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There are no teams followed by the user</br>- Geolocation is turned off|1) On the left sidebar menu, select <b>Team hub</b></br>2) Examine the team list|2) The list of news is empty|
</details>
