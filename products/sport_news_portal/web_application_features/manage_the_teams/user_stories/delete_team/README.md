### Back to [Manage teams on the portal](../../) feature

# Allow admin users to delete the existing team

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete an existing team

## Acceptance criteria

<pre>
Scenario: An admin user deletes an existing team
Given I am logged in as an admin user

When I hover over a table row
Then I see the trash icon next to the <b>Edit</b> link button

When I click the trash icon
Then I see the confirmation popup

When I click <b>Cancel</b>
Then I see a pop-up window disappears and nothing changes

When I click <b>Delete</b>
Then I see a success message
</pre>

## Mockups

1. Admin user sees trash icon on hover over the table row
2. Admin user sees delete team confirmation popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees trash icon on hover over the table row:**

![Admin user sees trash icon on hover over the table row](/products/sport_news_portal/web_application_features/manage_the_teams/images/edit_team_form.png)

**2. Admin user sees delete team confirmation popup:**

![Admin user sees delete team confirmation popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/delete_popup.png)

</details>

## Test cases

1. Verify that the trash icon appear on the right side of the Team section when hovering over a row
2. Verify the possibility to delete an existing team by clicking the trash icon on the right side of the team record
3. Verify the possibility to cancel of deleting an existing team

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the trash icon appear on the right side of the Team section when hovering over a row**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over a row|1) The trash icon appears on the right side next to the <b>Edit</b> link|

### **#2. Verify the possibility to delete an existing team by clicking the trash icon on the right side of the team record**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) Click the trash icon</br>3) Click <b>Delete</b> on the popup|2) The popover with a warning appears</br>3) The team is removed|

### **#3. Verify the possibility to cancel of deleting an existing team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) Click the trash icon</br>3) Click <b>Cancel</b> on the popup|2) The popover with a warning appears</br>3) The team is still present in the table|
</details>
