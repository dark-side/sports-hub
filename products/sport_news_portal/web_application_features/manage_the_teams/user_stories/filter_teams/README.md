### Back to [Manage teams on the portal](../../) feature

# Allow admin users to filter and search the teams

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to filter the teams page

## Acceptance criteria

<pre>
Scenario: An admin user views the <b>Teams</b> page and filters the existing teams
Given I am logged in as an admin user

When I view the <b>Teams</b> page
Then I see the button <b>+Add team</b> in the page header
  And I see the section with the map (with the <b>Reset, Zoom in</b> and <b>Zoom out</b> icons) on the left side and the filter form on the right that has the following elements:
    - Select location drop-down list box (default value "All")
    - Select category drop-down list box (default value "All")
    - Select subcategory drop-down list box (default value "All")
    - Team box
    - Apply button (disabled by default)
    - Cancel button (disabled by default)
  And I see the section with the list of existing teams in the table with the following:
    - Teams
    - Location
    - Added at
    - Category
    - Subcategory
  And I see all columns can be sorted by clicking on the title
  And I see a search field

When I click anywhere on the map
Then I see the <b>Select location</b> is filled in according to the selected location on the map

When I fill in filter drop-downs in the form on the right side of the map and click the <b>Apply</b> button
Then I see the teams in the list are filtered according to selected values in the drop-downs

When I click the <b>Cancel</b> button
Then I see filter drop-downs are cleared
  And I see all teams on the list

When I view the list of the teams
Then I see the pagination block in the bottom
  And I see the string with the total number of found teams
  And I see the <b>Result per page</b> field with the options: 10, 20, 45, 90

When I change the number in the <b>Result per page</b> field
Then I see the grid is refreshed according to the number

When I type team name in the search field
Then I see the table is refreshed with the matching results
</pre>

## Mockups

1. Admin user sees filter on the Teams page and Apply and Cancel button being disabled
2. Admin user sees filter on the Teams page and Apply and Cancel button being enabled

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees filter on the Teams page:**

![Admin user sees filter on the Teams page](/products/sport_news_portal/web_application_features/manage_the_teams/images/manage_teams_page.png)

**2. Admin user sees filter on the Teams page and Apply and Cancel button being enabled:**

![Admin user sees filter on the Teams page and Apply and Cancel button being enabled](/products/sport_news_portal/web_application_features/manage_the_teams/images/teams_page_active_filter_buttons.png)

</details>

## Test cases

1. Verify the block with the list of existing teams
2. Verify filtering of teams by the Apply button after completing the form
3. Verify filter cancelation
4. Verify the pagination of the teams table
5. Verify search of the teams table
6. Verify the possibility to select the location by clicking on the map

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the block with the list of existing teams**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page |1) Observe the content of the block with the list of existing teams|1) The block with the list of existing teams consists of such columns: <b>Teams, Location, Added at, Category, Subcategory</b>|

### **#2. Verify filtering of teams by the Apply button after completing the form**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Complete the filter form by selecting the needed data in every drop-down list</br>2) Click <b>Apply</b> button|2) The teams are filtered according to selected items in drop-down lists|

### **#3. Verify filter cancelation**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Complete the filter form by selecting the needed data in every drop-down list</br>2) Click Cancel|2) The form is reset and all teams are displayed|

### **#4. Verify the pagination of the teams table**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Click any page on the pagination block under the list of existing teams</br>2) Change Result per page number |1) Admin user is navigated to the chosen page of the table</br>2) The table renders the selected number of rows|

### **#5. Verify search of the teams table**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Click the search icon</br>2) Type something into the search field |2) The table renders the matching results|

### **#6. Verify the possibility to select the location by clicking on the map**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Teams</b> configuration page|1) Click on the <b>+Add team</b> button</br>2) Click anywhere on the map</br>3) Complete the form</br>4) Click <b>Add to list</b>|2) Select the Location dropdown is filled according to the selected location on the map</br>4) A success message appears and the team is added to the top of the list|
</details>