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

Given I am logged in as a site user

When I am on any page of the application
Then I see <b>Team hub</b> on the navigation menu

When I click <b>Team hub</b>
Then I see the list of news that is sorted according to the teams I selected in my personal cabinet
  And I see the <b>Most popular</b> and <b>Most commented</b> sections

When I click <b>Unfollow</b> any team
Then I see the confirmation pop-up window

When I confirm the action
Then I see the team news disappears from the page
And I see the message "You have unfollowed the team {team name}!"
</pre>

## Mockups

1. Users see the Team hub page
3. Users see Unfollow team confirmation pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Team hub page:**

![Users see the Team hub page](/products/sport_news_portal/web_application_features/team_hub/images/team_hub_page.png)

**2. Users see Unfollow team confirmation pop-up window:**

![Users see Unfollow team confirmation pop-up window](/products/sport_news_portal/web_application_features/team_hub/images/unfollow_team_confirmation_popup.png)

</details>

## Test cases

1. Verify content of the Team hub page
2. Verify the possibility to unfollow the team
3. Verify the possibility to cancel unfollowing

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify content of the Team hub page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are Team1 and Team2 followed by the user|1) Click <b>Team hub</b> in the navigation menu</br>2) Examine the page|2) There is news for each team followed by the user. There are <b>Most Popular</b> and <b>Most Commented</b> sections in case they are enabled by admin|

### **#2. Verify the possibility to unfollow the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some teams followed by the user|1) Click <b>Unfollow</b> for any team</br>2) On the confirmation pop-up window, click <b>Yes</b></br>3) Go to <b>My teams</b> list in Personal cabinet|2) The team section with news disappears from the page and the system displays the message "You have unfollowed the team {team name}!"</br>3) The removed team is not present on the list|

### **#3. Verify the possibility to cancel unfollowing**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There are some teams followed by the user|1) Click <b>Unfollow</b> for any team</br>2) On the confirmation pop-up window, click <b>No</b></br>3) Go to <b>My teams</b> list in Personal cabinet|2) The team section with news is still present on the page</br>3) The team is still present on the list|
</details>
