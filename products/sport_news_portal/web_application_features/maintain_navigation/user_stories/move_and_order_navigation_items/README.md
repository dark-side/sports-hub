### Back to [Maintain navigation on the portal](../../) feature

# Allow admin user to change order of the navigation menu items and move them between the categories and subcategories

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to change order of the navigation menu items and move them between the categories and subcategories

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user changes order of the navigation menu categories, subcategories, and teams and moves them between the categories and subcategories</i></b>

Given I am logged in as an admin user

When I am on the <b>Information architecture</b> configuration page
  And I select a category
Then I can drag and drop it up and down to change the order of the categories

When I select a subcategory
Then I can drag and drop it up and down to change the order of the subcategories inside the category
  And I can drag and drop it with all teams inside to any category

When I select the team
Then I can drag and drop it up and down to change the order of the teams inside the subcategory
  And I can drag and drop it to any subcategory of any category

When I hover over a category, subcategory, or team name
Then on the right of each category, subcategory, or team name, I see the ellipsis (<b>...</b>) button

When I click the ellipsis (<b>...</b>) button for any created category
Then I see the following options: <b>Delete</b>, <b>Edit</b>, and <b>Hide</b> category

When I click the ellipsis (<b>...</b>) button for any created subcategory or team
Then I see the following options: <b>Delete</b>, <b>Edit</b>, <b>Hide</b>, <b>Move</b> subcategory or team

When I click the ellipsis (<b>...</b>) button for static categories (<b>Lifestyle</b>, <b>Dealbook</b>, <b>Video</b>, <b>Team hub</b>)
Then I see an option <b>Hide</b> category

When I select a subcategory and click <b>Move</b>
Then I see a drop-down list with categories

When I select any category from the list
Then I see the subcategory with all teams inside is moved to the selected category
  And I see this subcategory at the top of the list of navigation menu subcategories for the selected category

When I select team and click <b>Move</b>
Then I see a menu with the list of categories and their subcategories where I can move the selected team

When I select any subcategory from the list
Then I see the team is moved to the selected subcategory
  And I see this team at the top of the list of the navigation menu teams for the selected subcategory in the category

When I click <b>Save</b> at the top of the page
Then I see changes applied to the category, subcategory, or team are saved
</pre>

## Mockups

1. Admin user sees actions for the subcategory
2. Admin user sees actions for the team
3. Admin user drag and drops the menu item to reorder
4. Admin user drag and drops the menu item to move
5. Admin user clicks <b>Save</b> and sees a flash message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the subcategory:**

![Admin user sees actions for the subcategory](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_subcategory_actions.png)

**2. Admin user sees actions for the team:**

![Admin user sees actions for the team](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_team_actions.png)

**3. Admin user drag and drops the menu item to reorder:**

![Admin user drag and drops the menu item to reorder](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_drag_and_drop_1.png)

**4. Admin user drag and drops the menu item to move:**

![Admin user drag and drops the menu item to move](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_drag_and_drop_2.png)

**5. Admin user clicks Save and sees a flash message:**

![Admin user clicks Save and sees a flash message](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_success_save.png)

</details>

## Test cases

1. Verify the ability to drag and drop a category to reorder categories
2. Verify that it is not possible to drag and drop a category inside other categories or inside subcategories or teams
3. Verify the ability to drag and drop a subcategory to reorder subcategories
4. Verify the ability to drag and drop a subcategory to another category
5. Verify that it is not possible to drag and drop a subcategory inside other subcategories or teams
6. Verify the ability to drag and drop a team to reorder teams
7. Verify the ability to drag and drop a team to another subcategory in any category
8. Verify that it is not possible to drag and drop a team inside other team or category

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the ability to drag and drop a category to reorder categories**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a category and drag and drop it up or down to change the order of categories|1) The order of the categories is changed|

### **#2. Verify that it is not possible to drag and drop a category inside other categories or inside subcategories or teams**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a category and drag and drop it to another category or to the subcategory or team|1) The category is back to the place from which it was moved|

### **#3. Verify the ability to drag and drop a subcategory to reorder subcategories**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a subcategory and drag and drop it up or down to change the order of subcategories|1) The order of the subcategories is changed|

### **#4. Verify the ability to drag and drop a subcategory to another category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a subcategory and drag and drop it to another category|1) The subcategory with all teams inside is moved to the selected category|

### **#5. Verify that it is not possible to drag and drop a subcategory inside other subcategories or teams**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a subcategory and drag and drop it to another subcategory or to the team|1) The subcategory is back to the place from which it was moved|

### **#6. Verify the ability to drag and drop a team to reorder teams**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a team and drag and drop it up or down to change the order of teams|1) The order of the teams is changed|

### **#7. Verify the ability to drag and drop a team to another subcategory in any category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a team and drag and drop it to another subcategory in any category|1) The team is moved to a selected subcategory in the selected category|

### **#8. Verify that it is not possible to drag and drop a team inside other team or category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) Select a team and drag and drop it to another team or to the category|1) The team is back to the place from which it was moved|

</details>
