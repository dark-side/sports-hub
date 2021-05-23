### Back to [Maintain navigation on the portal](../../) feature

# Allow admin user to create navigation menu items on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to create the navigation menu categories, subcategories, and teams visible to the site users

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user creates the navigation menu categories, subcategories, and teams</i></b>

Given I am logged in as an admin user

When I am on the <b>Information architecture</b> configuration page
Then I see the list of navigation menu categories and the <b>Save</b> button

When I click <b>+ Add category</b>
Then I see the <b>Add new category</b> popover with the <b>Name</b> field, the <b>Add</b> and <b>Cancel</b> buttons

When I click <b>Cancel</b>
Then I see the <b>Add new category</b> popover is closed
  And the category is not added

When I type the category name and click <b>Add</b>
Then I see the <b>Add new category</b> popover is closed
  And I see the new category item is created
  And I see this category at the top of the list of navigation menu categories

When I select the category name
Then I see the <b>+ Add subcategory</b> button on to the right of the <b>+ Add category</b>
  And I see systems displays list of the subcategories related to the selected category

When I click <b>+ Add subcategory</b>
Then I see the system shows <b>Add new subcategory</b> popover with the <b>Name</b> field, the <b>Add</b> and <b>Cancel</b> buttons

When I click <b>Cancel</b>
Then I see the <b>Add new subcategory</b> popover is closed
  And subcategory is not added

When I type the subcategory name and click <b>Add</b>
Then I see the <b>Add new subcategory</b> popover is closed
  And I see a new subcategory item is created
  And I see this created subcategory at the top of the list of navigation menu subcategories for the selected category

When I select the subcategory name
Then I see the <b>+ Add team</b> button on to the right of the <b>+ Add subcategory</b>
  And I see a list of the teams related to the selected subcategory

When I click <b>+ Add team</b>
Then I see the <b>Add new team</b> popover with the <b>Name</b> field, the <b>Add</b> and <b>Cancel</b> buttons

When I click <b>Cancel</b>
Then I see the <b>Add new team</b> popover is closed
  And the team is not added

When I type a team name and click <b>Add</b>
Then I see the <b>Add new team</b> popover is closed
  And I see a new team is created
  And I see this created team at the top of the list of navigation menu teams for the selected subcategory

When I hover over a category, subcategory, or team name
Then on the right of each category, subcategory, or team name, I see the ellipsis (<b>...</b>) button

When I click the ellipsis (<b>...</b>) button for any created category
Then I see the following options: <b>Delete</b>, <b>Edit</b>, and <b>Hide</b> category

When I click the ellipsis (<b>...</b>) button for any created subcategory or team
Then I see the following options: <b>Delete</b>, <b>Edit</b>, <b>Hide</b>, <b>Move</b> subcategory or team

When I click the ellipsis (<b>...</b>) button for static categories (<b>Lifestyle</b>, <b>Dealbook</b>, <b>Video</b>, <b>Team hub</b>)
Then I see an option <b>Hide</b> category

When I select a category, subcategory, or team and click <b>Delete</b>
Then I see the confirmation popover

When I confirm <b>Delete</b>
Then I see the selected category, subcategory, or team is deleted

When I select a category, subcategory, or team and click <b>Edit</b>
Then I see the edit pop-up window with the pre-populated name field

When I click <b>Save</b> in the pop-up window
Then the name is updated

When I click <b>Cancel</b> in the pop-up window
Then the name is not updated

When I click <b>Save</b> at the top of the page
Then I see changes applied to the category, subcategory, or team are saved
</pre>

## Mockups

1. Admin user sees default Information architecture configuration page
2. Admin user selects the category and sees subcategories
3. Admin user selects the subcategory and sees teams
4. Admin user sees actions for the subcategory and hidden NFL category
5. Admin user sees actions for the team
6. Admin user clicks to add the category and sees a pop-up window
7. Admin user clicks <b>Save</b> and sees a flash message
8. Admin user clicks <b>Delete</b> the subcategory and sees a pop-up window

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees default Information architecture configuration page:**

![Admin user sees default Information architecture configuration page](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_category_only.png)

**2. Admin user selects the category and sees subcategories:**

![Admin user selects the category and sees subcategories](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_subcategory_only.png)

**3. Admin user selects the subcategory and sees teams:**

![Admin user selects the subcategory and sees teams](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_with_team.png)

**4. Admin user sees actions for the subcategory and hidden NFL category:**

![Admin user sees actions for the subcategory and hidden NFL category](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_subcategory_actions.png)

**5. Admin user sees actions for the team:**

![Admin user sees actions for the team](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_team_actions.png)

**6. Admin user clicks to add the category and sees a pop-up window:**

![Admin user clicks to add the category and sees a pop-up window](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_new_category_popup.png)

**7. Admin user clicks Save and sees a flash message:**

![Admin user clicks Save and sees a flash message](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_success_save.png)

**8. Admin user clicks Delete the subcategory and sees a pop-up window:**

![Admin user clicks Delete the subcategory and sees a pop-up window](/products/sports_hub_portal/web_application_features/maintain_navigation/images/ia_delete_popup.png)

</details>

## Test cases

1. Verify if admin is able to add the new category
2. Verify if admin is able to cancel the adding of the new category
3. Verify if admin is able to add the new subcategory
4. Verify if admin is able to cancel the adding of the new subcategory
5. Verify if admin is able to add a new team
6. Verify if admin is able to cancel the adding of a new team
7. Verify the ability to delete the category
8. Verify the ability to delete the subcategory
9. Verify the ability to delete the team
10. Verify the ability to edit the category
11. Verify the ability to cancel editing the category
12. Verify the ability to edit the subcategory
13. Verify the ability to cancel editing the subcategory
14. Verify the ability to edit the team
15. Verify the ability to cancel editing the team

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify if admin is able to add the new category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Click <b>+ Add category</b></br>2) On the <b>Add new category</b> popover, in the <b>Name</b> box, enter a category name</br>3) Click <b>Add</b>|3) The new category is created and appears at the top of the categories list|

### **#2. Verify if admin is able to cancel the adding of the new category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Click <b>+ Add category</b></br>2) Click <b>Cancel</b>|2) The <b>Add new category</b> popover is closed. No category is added|

### **#3. Verify if admin is able to add the new subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a category name</br>2) Click <b>+ Add subcategory</b></br>3) On the <b>Add new subcategory</b> popover, in the <b>Name</b> box, enter the subcategory name</br>4) Click <b>Add</b>|1) The <b>+ Add subcategory</b> button appears on the right of the <b>+ Add category</b> button</br>4) The new subcategory is created and appears at the top of the subcategories list in the selected category|

### **#4. Verify if admin is able to cancel the adding of the new subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</Select>- Go to the <b>Information Architecture</b> configuration page|1) Select a category name</br>2) Click <b>+ Add subcategory</b></br>3) On the <b>Add new subcategory</b> popover, in the <b>Name</b> box, enter the subcategory name</br>4) Click <b>Cancel</b>|1) The <b>+ Add subcategory</b> button appears on the right of the <b>+ Add category</b> button</br>4) The <b>Add new subcategory</b> popover is closed. No subcategory is added|

### **#5. Verify if admin is able to add a new team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select the subcategory name</br>2) Click <b>+ Add team</b></br>3) On the <b>Add new team</b> popover, in the <b>Name</b> box, enter a team name</br>4) Click <b>Add</b>|1) The <b>+ Add team</b> button appears on the right of the <b>+ Add subcategory</b> button</br>4) The new team is created and appears at the top of the team list in the selected subcategory for the category|

### **#6. Verify if admin is able to cancel the adding of a new team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select the subcategory name</br>2) Click <b>+ Add team</b></br>3) On the <b>Add new team</b> popover, in the <b>Name</b> box, enter a team name</br>4) Click <b>Cancel</b>|1) The <b>+ Add team</b> button appears on the right of the <b>+ Add subcategory</b> button</br>4) The <b>Add new team</b> popover is closed. No team is added|

### **#7. Verify the ability to delete the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) On the right of any category, click the ellipsis (...) button</br>2) Click <b>Delete</b></br>3) Click <b>Delete</b>|2) Confirmation popover appears</br>3) The category is deleted|

### **#8. Verify the ability to delete the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) On the right of any subcategory, click the ellipsis (...) button</br>2) Click <b>Delete</b></br>3) Click <b>Delete</b>|2) Confirmation popover appears</br>3) The subcategory is deleted|

### **#9. Verify the ability to delete the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) On the right of any team, click the ellipsis (...) button</br>2) Click <b>Delete</b></br>3) Click <b>Delete</b>|2) Confirmation popover appears</br>3) The team is deleted|

### **#10. Verify the ability to edit the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is a category|1) On the right of a category, click the ellipsis (...) button</br>2) Click <b>Edit</b></br>3) Edit the name</br>4) Click <b>Save</b>|2) Popover with the category name, <b>Save</b> and <b>Cancel</b> buttons appears</br>4) Popover is closed and category saved in the same place with the new name and all subcategories and teams inside|

### **#11. Verify the ability to cancel editing the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is a category|1) On the right of a category, click the ellipsis (...) button</br>2) Click <b>Edit</b></br>3) Edit the name</br>4) Click <b>Cancel</b>|2) Popover with the category name, <b>Save</b> and <b>Cancel</b> buttons appears</br>4) Popover is closed and the category stays in the same place with the same name|

### **#12. Verify the ability to edit the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the subcategory|1) On the right of the subcategory, click the ellipsis (...) button</br>2) Click <b>Edit</b></br>3) Edit the name</br>4) Click <b>Save</b>|2) Popover with the subcategory name, <b>Save</b> and <b>Cancel</b> buttons appears</br>4) Popover is closed and subcategory saved in the same place with the new name and all teams inside|

### **#13. Verify the ability to cancel editing the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the subcategory|1) On the right of the subcategory, click the ellipsis (...) button</br>2) Click <b>Edit</b></br>3) Edit the name</br>4) Click <b>Cancel</b>|2) Popover with the subcategory name, <b>Save</b> and <b>Cancel</b> buttons appears</br>4) Popover is closed and the subcategory stays in the same place with the not changed name|

### **#14. Verify the ability to edit the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the team|1) On the right of the team, click the ellipsis (...) button</br>2) Click <b>Edit</b></br>3) Edit the name</br>4) Click <b>Save</b>|2) Popover with the team name, <b>Save</b> and <b>Cancel</b> buttons appears</br>4) Popover is closed and team saved in the same place with the new name|

### **#15. Verify the ability to cancel editing the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the team|1) On the right of the team, click the ellipsis (...) button</br>2) Click <b>Edit</b></br>3) Edit the name</br>4) Click <b>Cancel</b>|2) Popover with the team name, <b>Save</b> and <b>Cancel</b> buttons appears</br>4) Popover is closed and the team stays in the same place with the same name|

</details>
