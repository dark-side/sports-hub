### Back to [Manage teams on the portal](../../README.md) feature

# Allow admin users to delete the existing team

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete the existing team

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes the existing team</i></b>

Given I am logged in as an admin user

When I hover over a table row
Then I see the trash icon next to the <b>Edit</b> link button

When I click the trash icon
Then I see the confirmation pop-up window

When I click <b>Cancel</b>
Then I see a pop-up window disappears and nothing changes

When I click <b>Delete</b>
Then I see a success message
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the trash icon on hovering over the table row
2. Admin user sees the delete team confirmation pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the trash icon on hovering over the table row:**

![Admin user sees the trash icon on hovering over the table row](/desktop_application_features/maintain_navigation/images/edit_team_form.png)

**2. Admin user sees the delete team confirmation pop-up window:**

![Admin user sees the delete team confirmation pop-up window](/desktop_application_features/maintain_navigation/images/delete_popup.png)

</details>

## Test cases

1. Verify that the trash icon appears on the right side of the <b>Team</b> section when hovering over a row
2. Verify the possibility to delete existing teams by clicking the trash icon on the right side of the team record
3. Verify the possibility to cancel deleting of existing teams

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the trash icon appears on the right side of the Team section when hovering over a row**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over a row|1) The trash icon appears on the right side next to the <b>Edit</b> link|

### **#2. Verify the possibility to delete existing teams by clicking the trash icon on the right side of the team record**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) Click the trash icon</br>3) Click <b>Delete</b> in the pop-up window|2) The popover with a warning appears</br>3) The team is removed|

### **#3. Verify the possibility to cancel deleting of existing teams**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Hover over any team row</br>2) Click the trash icon</br>3) Click <b>Cancel</b> in the pop-up window|2) The popover with a warning appears</br>3) The team is still present in the table|
</details>
