### Back to [Maintain navigation on the portal](../../) feature

# Allow site users to navigate to the sports categories, subcategories, and teams page on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view the navigation menu on every page of the Sports Hub site
    So that I can navigate between sports categories, subcategories, and teams news pages

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the navigation menu on every page of the Sports Hub site</i></b>

Given I am a site user

When I view any page on the site
Then I see the main navigation menu in the left sidebar with the default and configured categories
  And I see these categories appear in the order configured by admin

When I select any navigation menu category
Then I am taken to the landing news page for that sports category
  And I see that category item has active state (highlighted) in the sidebar

When I hover over on any navigation menu category
Then I see the second navigation menu with the subcategories available in that category
  And I see these subcategories appear in the order configured by admin

When I select the second navigation menu subcategory item
Then I am taken to the landing news page for that subcategory
  And I see a corresponding navigation menu category item has active state (highlighted) in the sidebar

When I hover over any of the subcategories in the navigation menu
Then I see the third list of the teams available in that subcategory
  And I see these teams appear in the order configured by admin

When I select any team
Then I am taken to the landing news page for that team

When I view a team page of the site
Then I see a corresponding navigation menu category item has an active state (highlighted) in the sidebar
</pre>

## Mockups

1. User hovers over the category in the navigation menu
2. User hovers over the subcategory in the navigation menu

<details>
  <summary>Click here to see mockups details</summary>

**1. User hovers over the category in the navigation menu:**

![User hovers over the category in the navigation menu](/products/sports_hub_portal/web_application_features/maintain_navigation/images/category_user_hover.png)

**2. User hovers over the subcategory in the navigation menu:**

![User hovers over the subcategory in the navigation menu](/products/sports_hub_portal/web_application_features/maintain_navigation/images/subcategory_user_hover.png)

</details>

## Test cases

1. Verify selecting a navigation menu category
2. Verify the category submenu
3. Verify selecting the navigation menu subcategory item
4. Verify a secondary navigation dropdown of subcategory
5. Verify selecting the team menu

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify selecting a navigation menu category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to any page|1) Select any navigation menu category</br>2) Check sports category|1) The user is navigated to the landing page for that sports category</br>2) The corresponding navigation menu category item has an active state (highlighted)|

### **#2. Verify the category submenu**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Hover over any sports category</br>2) Check the list of subcategories in that category|1) Navigation submenu opens</br>2) The configured subcategories list displays|

### **#3. Verify selecting the navigation menu subcategory item**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Select any navigation menu subcategory item</br>2) Check a page within a subcategory of the site|2) The corresponding navigation menu category item has an active state (highlighted)|

### **#4. Verify a secondary navigation dropdown of subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Hover over any subcategory</br>2) In that subcategory, check the list of teams|2) The configured teams list displays|

### **#5. Verify selecting the team menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Select any team in the subcategory</br>2) Check a team news page|2) The corresponding navigation menu category item has an active state (highlighted)|

</details>
