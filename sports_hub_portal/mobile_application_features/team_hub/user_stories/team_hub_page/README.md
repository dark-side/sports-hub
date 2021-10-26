### Back to [Team hub: news about favorite teams](../../) feature

# Allow users to see the Team hub page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to go to the Team hub page
    So that I can read news about my favorite teams

## Acceptance criteria

<pre>
<b><i>Scenario: A logged-in user visits the Team hub page</i></b>

Given I am logged in as a user

When I am on any page of the application
Then I see the menu icon in the left upper corner

When I tap the menu icon
Then I see one of submenu items is the <b>Team hub</b> item

When I tap <b>Team hub</b>
Then I see the list of news that are sorted according to the teams I selected in the <b>Team hub</b> configuration page
  And I see the Most popular and Most commented sections
  And I see a list of team news contains 3 recent news and the <b>Unfollow</b> button

When I tap <b>Unfollow</b>
Then I see a confirmation popup

When I tap to confirm
Then I see the team news disappears from the <b>Team hub</b> page
</pre>

## Mockups

1. Users see <b>Team hub</b> in the navigation menu
2. Users see news on the <b>Team hub</b> page
3. Users see a confirmation popup
4. Full <b>Team hub</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Team hub in the navigation menu:**

![Users see Team hub in the navigation menu](/sports_hub_portal/mobile_application_features/team_hub/images/application_navigation_menu.png)

**2. Users see news on the Team hub page:**

![Users see news on the Team hub page](/sports_hub_portal/mobile_application_features/team_hub/images/application_team_hub_page.png)

**3. Users see a confirmation popup:**

![Users see a confirmation popup](/sports_hub_portal/mobile_application_features/team_hub/images/application_team_unfollow_confirmation.png)

**4. Full Team hub page:**

![Full Team hub page](/sports_hub_portal/mobile_application_features/team_hub/images/team_hub_full_page.png)

</details>

## Test cases

1. Verify that it is possible to unfollow the team from the <b>Team Hub</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that it is possible to unfollow the team from the Team Hub page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are some teams followed by the user</br>- The user is logged in</br>- User is on the <b>Team hub</b> page|1) Tap <b>Unfollow</b> for any team</br>2) Tap confirm|1) Confirmation popup arrears</br>2) The team news disappear from the page|

</details>
