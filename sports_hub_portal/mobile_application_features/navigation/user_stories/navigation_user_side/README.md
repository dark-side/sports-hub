### Back to [Navigation in the application](../../README.md) feature

# Allow users to navigate to the sports categories, subcategories, and teams page in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view the navigation menu on every page of the Sports Hub application
    So that I can navigate between sports categories, subcategories, and teams news pages

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the navigation menu on every page of the Sports Hub application</i></b>

Given I am a user

When I view any page
Then I see the main navigation menu icon in the left top corner

When I tap the main menu icon
Then the menu appears with the following categories:
  - Home
  - Category1
  - Category2
  - ...
  - CategoryN
  - Team hub
  - Lifestyle
  - Dealbook
  - Video
  - Language icons

When I select any navigation menu category
Then I am taken to the landing page for that sports category

When I select any navigation menu item arrow (arrow for some category)
Then I see the opened menu with the subcategories available in that category

When I select the navigation menu subcategory item
Then I am taken to the landing page for that subcategory

When I select any navigation menu subcategories arrow
Then I see the menu list with the teams available in that subcategory

When I select a team
Then I am taken to the landing page for that team
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a navigation menu
2. Users see navigation submenus

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a navigation menu:**

![Users see a navigation menu](/sports_hub_portal/mobile_application_features/navigation/images/application_main_navigation.png)

**2. Users see navigation submenus:**

![Users see navigation submenus](/sports_hub_portal/mobile_application_features/navigation/images/application_subcategory_navigation.png)

</details>

## Test cases

1. Verify tapping a navigation menu category
2. Verify the Category expanded menu
3. Verify a secondary navigation dropdown of subcategory
4. Verify tap on the Team menu

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify tapping a navigation menu category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to any page|1) Select any navigation menu category|1) The user is navigated to the landing page for that sports category|

### **#2. Verify the category submenu**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Select some sports category arrow</br>2) Check the list of subcategories in the sports category|2) List of subcategories is present|

### **#3. Verify a secondary navigation dropdown of subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Tap the subcategory arrow icon|1) The list of teams appears|

### **#4. Verify tap on the Team menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the main navigation menu|1) Select any team in the subcategory|1) The user is redirected to the appropriate team page|

</details>
