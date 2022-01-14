### Back to [Manage teams on the portal](../../) feature

# Allow admin users to add a new team on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to add a new team

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user adds a new team</i></b>

Given I am logged in as an admin user

When I click the <b>+ Add team</b> button
Then I see a new form next to the map, that consists of the following elements:
  - <b>Select location</b> drop-down list
  - <b>Select category</b> drop-down list
  - <b>Select subcategory</b> drop-down list
  - <b>Team</b> field
  - The box for uploading the team logo with the <b>Add logo</b> button
  - The <b>Add to list</b> button
  - The <b>Cancel</b> button

When I click anywhere on the map
Then I see the <b>Select location</b> drop-down list is filled in according to the selected location on the map

When I add a logo and hover over it
Then I see the box for uploading a team logo with the <b>Add logo</b> button

When I complete the form and click the <b>Add to list</b> button
Then I see a success message

When I click <b>Cancel</b>
Then I see the default form
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees a new team form
2. Admin user selects a logo in the form
3. Admin user sees a success message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a new team form:**

![Admin user sees a new team form](/sports_hub_portal/desktop_application_features/manage_the_teams/images/new_team_form.png)

**2. Admin user selects a logo in the form:**

![Admin user selects a logo in the form](/sports_hub_portal/desktop_application_features/manage_the_teams/images/new_team_form_with_logo.png)

**3. Admin user sees a success message:**

![Admin user sees a success message](/sports_hub_portal/desktop_application_features/manage_the_teams/images/success_message.png)

</details>

## Test cases

1. Verify the possibility to add the team by <b>+Add team</b> button on the <b>Teams</b> page
2. Verify the possibility to cancel adding the team on the <b>Teams</b> page
3. Verify the possibility to select the location by clicking the map

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to add the team by +Add team button on the Teams page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Click the <b>+Add team</b> button</br>2) Complete the form and click <b>Add to list</b>|2) A success message appears and the team is added to the top of the list|

### **#2. Verify the possibility to cancel adding the team on the Teams page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Click the <b>+Add team</b> button</br>2) Complete the form</br>3) Click <b>Cancel</b>|3) The default form for viewing teams appears|

### **#3. Verify the possibility to select the location by clicking the map**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Teams</b> configuration page|1) Click the <b>+Add team</b> button</br>2) Click anywhere on the map</br>3) Complete the form</br>4) Click <b>Add to list</b>|2) Select location drop-down list is filled according to the selected location on the map</br>4) A success message appears and the team is added to the top of the list|

</details>
