### Back to [Manage teams on the portal](../../) feature

# Allow admin users to add a new team in the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
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
  - Select location drop-down list
  - Select category drop-down list
  - Select subcategory drop-down list
  - Team field
  - The box for uploading the team logo with the <b>Add logo</b> button
  - <b>Add to list</b> button
  - <b>Cancel</b> button

When I click anywhere on the map
Then I see the <b>Select location</b> is filled in according to the selected location on the map

When I add a logo and hover over it
Then I see the box for uploading a team logo with the <b>Add logo</b> button

When I complete the form and click the <b>Add to list</b> button
Then I see a success message

When I click <b>Cancel</b>
Then I see the default form
</pre>

## Mockups

1. Admin user sees a new team form
2. Admin user selected a logo in the form
3. Admin user sees a success message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a new team form:**

![Admin user sees a new team form](/products/sport_news_portal/web_application_features/manage_the_teams/images/new_team_form.png)

**2. Admin user selected a logo in the form:**

![Admin user selected a logo in the form](/products/sport_news_portal/web_application_features/manage_the_teams/images/new_team_form_with_logo.png)

**3. Admin user sees a success message:**

![Admin user sees a success message](/products/sport_news_portal/web_application_features/manage_the_teams/images/success_message.png)

</details>

## Test cases

1. Verify the possibility to add team by +Add team button on the Teams page
2. Verify the possibility to cancel adding the team on the Teams page
3. Verify the possibility to select the location by clicking on the map

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to add team by +Add team button on the Teams page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Click on the <b>+Add team</b> button</br>2) Complete the form and click <b>Add to list</b>|2) A success message appears and the team is added to the top of the list|

### **#2. Verify the possibility to cancel adding the team on the Teams page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Click on the <b>+Add team</b> button</br>2) Complete the form</br>3) Click <b>Cancel</b>|3) The default form for viewing teams is shown|

### **#3. Verify the possibility to select the location by clicking on the map**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Click on the <b>+Add team</b> button</br>2) Click anywhere on the map</br>3) Complete the form</br>4) Click <b>Add to list</b>|2) Select the Location dropdown is filled according to the selected location on the map</br>4) A success message appears and the team is added to the top of the list|

</details>
