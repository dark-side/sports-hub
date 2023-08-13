### Back to [Team hub: news about favorite teams](../../README.md) feature

# Allow users to see teams news on Team hub based on their geolocation

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to read news about teams from my geolocation on the Team hub page when I haven’t configured favorite teams

## Acceptance criteria

<pre>
<b><i>Scenario: A logged-in users reads news about teams from their geolocation on the Team hub page</i></b>

Given I am logged in as a site user

When I am on the <b>Team hub</b> page and I haven’t configured my favorite teams in the personal cabinet
Then I see a list of news that are sorted according to the teams that are selected automatically based on my geolocation
</pre>


## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the Team hub page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Team hub page:**

![Users see the Team hub page](/web_application_features/team_hub/images/team_hub_geolocation_teams.png)

</details>

## Test cases

1. Verify that the team list on the Team hub page is selected automatically based on my geolocation
2. Verify that the team list on the Team hub page is empty if geolocation is turned off

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the team list on the Team hub page is selected automatically based on my geolocation**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are no teams followed by the user</br>- Geolocation is turned on|1) Select <b>Team hub</b> on the left sidebar menu</br>2) Examine the team list|2) There are news for each team that belongs to the user’s geolocation. There are the <b>Most Popular</b> and <b>Most Commented</b> sections in case they are enabled by admin|

### **#2. Verify that the team list on the Team hub page is empty if geolocation is turned off**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are no teams followed by the user</br>- Geolocation is turned off|1) Select <b>Team hub</b> on the left sidebar menu</br>2) Examine the team list|2) The list of news is empty|
</details>
