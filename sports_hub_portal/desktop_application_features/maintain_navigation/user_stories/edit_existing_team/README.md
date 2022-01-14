### Back to [Manage teams on the portal](../../) feature

# Allow admin users to edit the existing team

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to edit the existing team

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user edits the existing team</i></b>

Given I am logged in as an admin user

When I hover over a table row
Then I see the <b>Edit</b> link button on the right side

When I double-click a table row or click the <b>Edit</b> link button
Then I see the edit form next to the map is filled with the selected team details
  And I see the <b>Save</b> button that is disabled by default and the <b>Cancel</b> button

When I make changes
Then I see the <b>Save</b> button becomes enabled

When I hover over the logo
Then I see the box for uploading the team logo with the <b>Add logo</b> link

When I make the changes and click <b>Save</b>
Then I see a success message "The team is successfully updated"

When I click <b>Cancel</b>
Then I see the default form
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Edit</b> button on hover over the table row and edit form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Edit button on hover over the table row and edit form:**

![Admin user sees the Edit button on hover over the table row and edit form](/sports_hub_portal/desktop_application_features/manage_the_teams/images/edit_team_form.png)

</details>

## Test cases

1. Verify that the <b>Edit</b> button appears on the right side of the team when hovering over a row
2. Verify the possibility to edit existing teams by clicking the <b>Edit</b> button on the right side of a team
3. Verify the possibility to edit location for existing teams by clicking the map
4. Verify the possibility to cancel editing of existing teams by clicking the <b>Edit</b> button on the right side of a team record

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Edit button appears on the right side of the team when hovering over a row**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over a row|1) The <b>Edit</b> button appears on the right side|

### **#2. Verify the possibility to edit existing teams by clicking the Edit button on the right side of a team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) On the right side of the team row, click the <b>Edit</b> button</br>3) Enter new data to all fields</br>4) Click <b>Save</b>|2) The edit form next to the map appears with the <b>Save</b> button that is disabled by default and the <b>Cancel</b> button</br>4) All new data is saved as the team information|

### **#3. Verify the possibility to edit location for existing teams by clicking the map**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) On the right side of the team row, click the <b>Edit</b> button</br>3) Click anywhere on the map</br>4) Click <b>Save</b>|2) The edit form next to the map appears with the <b>Save</b> button that is disabled by default and the <b>Cancel</b> button</br>3) <b>Select location</b> drop-down list is changed according to the selected location on the map</br>4) All new data is saved as the team information|

### **#4. Verify the possibility to cancel editing of existing teams by clicking the Edit button on the right side of a team record**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) Click <b>Edit</b> on the right side of the team record</br>3) Update all fields with new data</br>4) Click <b>Cancel</b>|2) The edit form next to the map appears with the <b>Save</b> button that is disabled by default and the <b>Cancel</b> button</br>4) All old data is shown as the team information|

</details>
