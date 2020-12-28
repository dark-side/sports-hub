### Back to [Team hub - news of favorite teams](../../) feature

# Allow users to see Team Hub page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a logged-in user
    I want to go to the Team hub page
    So that I can read news of my favorite teams

## Acceptance criteria

<pre>
Scenario: A logged-in user visits the Team hub page
Given I am logged in as a site user

When I am on any page of the application
Then I see <b>Team hub</b> on the navigation menu

When I click <b>Team hub</b>
Then I see the list of news that are sorted according to the teams I selected in my personal cabinet
  And I see the <b>Most popular</b> and <b>Most commented</b> sections

When I click <b>Unfollow</b> any team
Then I see the confirmation pop-up window

When I confirm the action
Then I see the team news disappears from the page
And I see the message "You have unfollowed the team {team name}!"
</pre>

## Mockups

1. User sees Team Hub page
3. User sees Unfollow team confirmation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Team Hub page:**

![User sees Team Hub page](/products/sport_news_portal/web_application_features/team_hub/images/team_hub_page.png)

**2. User sees Unfollow team confirmation popup:**

![User sees Unfollow team confirmation popup](/products/sport_news_portal/web_application_features/team_hub/images/unfollow_team_confirmation_popup.png)

</details>

## Test cases

1. Verify content of Team hub page
2. Verify possibility to unfollow team
3. Verify possibility to cancel of unfollowing

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify content of Team hub page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There are Team1 and Team2 followed by the user|1) Click <b>Team hub</b> in the navigation menu</br>2) Examine the page|2) There are news for each team followed by the user. There are <b>Most Popular</b> and <b>Most Commented</b> sections in case they are enabled by admin|

### **#2. Verify possibility to unfollow team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There are some teams followed by user|1) Click <b>Unfollow</b> for any team</br>2) On the confirmation pop-up window, click <b>Yes</b></br>3) Go to <b>My teams</b> list in Personal cabinet|2) The team section with news disappears from the page and the system displays the message "You have unfollowed the team {team name}!"</br>3) The removed team is not present in the list|

### **#3. Verify possibility to cancel of unfollowing**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There are some teams followed by user|1) Click <b>Unfollow</b> for any team</br>2) On the confirmation pop-up window, click <b>No</b></br>3) Go to <b>My teams</b> list in Personal cabinet|2) The team section with news is still present on the page</br>3) The team is still present in the list|
</details>
