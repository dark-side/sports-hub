### Back to [Manage teams on the portal](../../) feature

# Allow admin users to view Teams page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to view Teams page
    So that I can see a map with the location of the existing teams and a list of the teams

## Acceptance criteria

    Scenario: An admin user views the Teams page and the map with the location of the existing teams
    Given I am logged in as an admin user

    When I view Teams page
    Then I see the button +Add Team/Player in the top of the page (in the right side from the title Teams)
      And I see the block with the map (with reset, zoom in and zoom out icons) on the left side and the form on the right side next to the map that consists of the next elements:
        - Select Location drop-down field (default value “All”)
        - Select Sports category drop-down field (default value “All”)
        - Select Subcategory drop-down field (default value “All”)
        - Team/Player field
        - Apply button
        - Cancel button
      And I see the block with the list of existing teams that is presented as a grid with next columns:
        - Teams/Players
        - Location
        - Date Added
        - Sport Category
        - Subcategory
      And I see all columns can be sorted clicking on the title
    When I hover the row
    Then I see Edit link in the right side
      And I see Trash icon next to the Edit link
    When I complete the form and click the Apply button
    Then I see the teams in the list based on filters values in the form
    When I click the Cancel button
    Then I see the form will be reset
      And I see all teams in the list
    When I view the list of the teams
    Then I see the pagination block in the bottom
      And I see the string with total number of found teams
      And I see the select field with the number of teams represented in the grid, next to the string
    When I change the number in the select field
    Then I see the grid is refreshed according to the entered number

## Mockups

1. User sees teams page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees teams page:**

![Teams page Screen](/products/sport_news_portal/web_application_features/manage_the_teams/images/teams_page.png)

</details>

## Test Scenarios

1. Verify the content of Teams page
2. Verify the content of Selection form
3. Verify the block with the list of existing teams
4. Verify Edit link and Trash icon in the right side of the Team/Players block
5. Verify Apply Button after completing the form
6. Verify Cancel Button after completing the form
7. Verify the pagination block
8. Verify the string with total number of found teams

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of Teams page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the content of Teams page|Teams page consists of<br>- the block with the map (with reset, zoom in and zoom out icons) on the left side<br>- the form on the right side next to the map

### **#2. Verify the content of Selection form**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the content of Selection form on the right side next to the map|Selection form consists of:<br>- Select Location drop-down field (default value "All")<br>- Select Sports category drop-down field (default value "All")<br>- Select Subcategory drop-down field (default value "All")<br>- Team/Player field<br>- Apply button

### **#3. Verify the block with the list of existing teams**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the content of the block with the list of existing teams|The block with the list of existing teams consists of such columns:<br>- Teams/Players<br>- Location<br>- Date Added<br>- Sport Category<br>- Subcategory

### **#4. Verify Edit link and Trash icon in the right side of the Team/Players block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the content of the block with the list of existing teams|The block with the list of existing teams consists of such columns:<br>- Teams/Players<br>- Location<br>- Date Added<br>- Sport Category<br>- Subcategory
|5|Hovers the row|Edit link and Trash icon appears in the right side

### **#5. Verify Apply Button after completing the form**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the content of the block with the list of existing teams|The block with the list of existing teams consists of such columns:<br>- Teams/Players<br>- Location<br>- Date Added<br>- Sport Category<br>- Subcategory
|5|Complete the form choosing needed data in every dropdown list|
|6|Click Apply|The teams are displayed in the list based on filters values previously chosen in the form

### **#6. Verify Cancel Button after completing the form**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the content of the block with the list of existing teams|The block with the list of existing teams consists of such columns:<br>- Teams/Players<br>- Location<br>- Date Added<br>- Sport Category<br>- Subcategory
|5|Complete the form choosing needed data in every dropdown list|
|6|Click Cancel|The form is reset

### **#7. Verify the pagination block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click any page on the the pagination block under the list of existing teams|Admin user is navigated to chosen page

### **#8. Verify the string with total number of found teams**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Observe the string with total number of found teams|
|5|Change the number in the select field|The grid will be refreshed according to the entered number

</details>
