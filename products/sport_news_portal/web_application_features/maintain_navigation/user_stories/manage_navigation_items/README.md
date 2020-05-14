### Back to [Maintain Navigation on the portal](/../../) feature

# Allow admin users to manage navigation items on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to configure the Navigation menu categories, subcategories and teams
    So that I have control over the sport categories, subcategories and teams visible to the site users

## Acceptance criteria

    Scenario: An admin site configures the Navigation menu categories, subcategories and teams
    Given I am logged in as an admin user

    When I am on Information Architecture configuration page, 
    Then I see list of Navigation Menu Categories and Add category button
    When I click on Add category button
    Then I see a Add new category modal with an input for category name and Add and Cancel buttons
    When I click the Cancel button
    Then I see a Add new category modal is closed
    When I fill in category name input and click the Add button
    Then I see a new category item is created 
      And I see the Add new category modal is closed 
      And I see system displays this created category item in the list of Navigation Menu Categories
    When I click on the category name
    Then I see a Add sub category button appears to the right of the Add new category button
      And I see systems displays list of the subcategories related to the selected category
    When I click on Add sub category button
    Then I see system shows Add new subcategory modal with an input for subcategory name and Add and Cancel buttons
    When I click the Cancel button
    Then I see a Add new subcategory modal is closed
    When I fill in subcategory name input and click the Add button
    Then I see a new subcategory item is created 
      And I see the Add new subcategory modal is closed 
      And I see this created subcategory item in the list of Navigation Menu Subcategories list
    When I click on the subcategory name
    Then I see a Add team button appears to the right of the Add new subcategory button
      And I see list of the teams related to the selected subcategory
    When I click on Add team button
    Then I see a Add new team modal with an input for team name and Add and Cancel buttons
    When I click the Cancel button
    Then I see a Add new team modal is closed
    When I fill in team name input and click the Add button
    Then I see a new team is created 
      And I see the Add new team modal is closed 
      And I see this created team in the list of Navigation Menu Teams list
    When I click on the category, subcategory or team name 
    Then I can drag and drop it up or down to change the order of the category/ subcategory/ team
    When I hover over the category, subcategory or team name
    Then I see a three dots to the right of the category/ subcategory/ team name
    When I click on this three dots 
    Then I see an options to delete or hide category (in case of clicking on the category) and option to delete, move or hide the subcategory/ team (in case I click on the subcategory/ team)
    Note: The delete option is not available for LIFESTYLE, DEALBOOK, VIDEO and TEAM HUB categories as they are static
    When I click on Delete option
    Then I see  selected category/ subcategory/ team is deleted
    When I click on Hide option
    Then I see selected category/ subcategory/ team is hidden (not displayed on the UI, but not removed from the database)
    When I click on Move option for the subcategory
    Then I see a dropdown with list of categories
    When I select any category from the list
    Then I see a subcategory is moved to the selected category
    When I click on Move option for the team
    Then I see a menu with list of categories and their subcategories where I can move the selected team 
    When I select a subcategory from this list
    Then I see a team is moved to the selected subcategory
    When I click a Save button
    Then I see changes applied to the categories/ subcategories/ teams are saved

## Mockups

1. Admin user sees Add New Category/Subcategory/Team modal 
2. Admin user sees configuration page for Navigation Menu
3. Admin user drags and drops Category/Subcategory/Team
4. Admin user sees menu with Move/Hide/Delete actions for subcategory
5. Admin user sees menu with Move/Hide/Delete actions for team

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Add New Category/Subcategory/Team modal:**

![Add New Category/Subcategory/Team modal](/products/sport_news_portal/web_application_features/maintain_navigation/images/add_new_category_subcategory_team_modal.png)

**2. Admin user sees configuration page for Navigation Menu:**

![Configuration page for Navigation Menu](/products/sport_news_portal/web_application_features/maintain_navigation/images/admin_configuration_page_for_navigation_menu.png)

**3. Admin user drags and drops Category/Subcategory/Team:**

![Drag and drop Category/Subcategory/Team](/products/sport_news_portal/web_application_features/maintain_navigation/images/drag_and_drop_category_subcategory_team.png)

**4. Admin user sees menu with Move/Hide/Delete actions for subcategory:**

![Move/Hide/Delete subcategory](/products/sport_news_portal/web_application_features/maintain_navigation/images/move_hide_delete_subcategory.png)

**5. Admin user sees menu with Move/Hide/Delete actions for team:**

![Move/Hide/Delete team](/products/sport_news_portal/web_application_features/maintain_navigation/images/move_hide_delete_team.png)

</details>

## Test Scenarios

1. Verify list of Navigation Menu Categories
2. Verify clicking on Add category button
3. Verify clicking on Cancel button on adding new category
4. Verify Add sub category button
5. Verify adding new sub category
6. Verify clicking on cancel button on adding new sub category
7. Verify clicking on Add team button
8. Verify ability to drag and drop the Category
9. Verify ability to drag and drop the Subcategory
10. Verify ability to drag and drop the Team
11. Verify ability to delete the Category
12. Verify ability to delete the Subcategory
13. Verify ability to delete the Team

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify list of Navigation Menu Categories**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Observe the list of Navigation Menu Categories|List of Navigation Menu Categories is present on Information Architecture configuration page

### **#2. Verify clicking on Add category button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on Add category button|System shows Add new category modal with an input for category name
|4|Fill in the category name|
|5|Click add|The new category item is created

### **#3. Verify clicking on Cancel button on adding new category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on Add category button|
|4|Click on Cancel button|The Add new category modal is closed

### **#4. Verify Add sub category button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on the category name|The Add sub category button appears to the right of the Add new category button

### **#5. Verify adding new sub category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on add sub category button|
|5|Fill in sub category name input and click|
|6|Click add|The system displays this created subcategory item in the list of Navigation Menu

### **#6. Verify clicking on cancel button on adding new sub category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on add sub category button|
|5|Click Cancel|The Add new subcategory modal is closed

### **#7. Verify clicking on Add team button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Сlick on the subcategory name|The Add team button appears to the right of the Add new subcategory button a list of the teams related to the selected subcategory is displayed
|5|Click on Add team button|System shows Add new team modal with an input for team name
|6|I fill in team name input|
|7|Click on the Add button|The new team is created and the Add new team modal is closed. The system displays this created team in the list of Navigation Menu Teams list

### **#8. Verify ability to drag and drop the Category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on the category and drag and drop it up or down to change the order of the category|The order of the category can be changed

### **#9. Verify ability to drag and drop the Subcategory**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on the subcategory and drag and drop it up or down to change the order of the subcategories|The order of the subcategories can be changed

### **#10. Verify ability to drag and drop the Team**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on the Team and drag and drop it up or down to change the order of the Teams|The order of the Teams can be changed

### **#11. Verify ability to delete the Category**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on three dots to the right of the Category|
|5|Click on Delete|The order of the Category can be deleted 

### **#12. Verify ability to delete the Subcategory**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on three dots to the right of the Subcategory|An option to delete a team is present
|5|Click on Delete|Chosen Subcategory is deleted

### **#13. Verify ability to delete the Team**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Go to Information Architecture configuration page|
|4|Click on three dots to the right of the Team|An option to delete a team is present
|5|Click on Delete|Chosen Team is deleted

</details>

