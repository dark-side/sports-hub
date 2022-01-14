### Back to [Maintain navigation on the portal](../../) feature

# Allow admin user to show and hide navigation menu items on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to show and hide the navigation menu categories, subcategories, and teams on the portal

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user shows or hides the navigation menu categories, subcategories, and teams</i></b>

Given I am logged in as an admin user

When I am on the <b>Information architecture</b> configuration page
Then I see the list of navigation menu categories and the <b>Save</b> button

When I hover over a category, subcategory, or team name
Then on the right of each category, subcategory, or team name, I see the ellipsis (<b>...</b>) button

When I click the ellipsis (<b>...</b>) button for any created category
Then I see the following options: <b>Delete</b>, <b>Edit</b>, and <b>Hide</b> (<b>Show</b>) category

When I click the ellipsis (<b>...</b>) button for any created subcategory or team
Then I see the following options: <b>Delete</b>, <b>Edit</b>, <b>Hide</b> (<b>Show</b>), <b>Move</b> subcategory or team

When I click the ellipsis (<b>...</b>) button for static categories (<b>Lifestyle</b>, <b>Dealbook</b>, <b>Video</b>, <b>Team hub</b>)
Then I see an option <b>Hide</b> category

When I click <b>Hide</b> not hidden category, subcategory, or team
Then I see selected category, subcategory, or team is not displayed on the users UI
  And the "Hidden" label is shown for that category, subcategory, or team on the <b>Information architecture</b> configuration page

When I click <b>Show</b> a hidden category, subcategory, or team
Then I see the selected category, subcategory, or team is displayed on the users UI
  And the "Hidden" label is not shown anymore for that appropriate category, subcategory, or team on the <b>Information architecture</b> configuration page

When I click <b>Save</b> at the top of the page
Then I see changes applied to the category, subcategory, or team are saved
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions for the subcategory and hidden label for the NFL category
2. Admin user sees actions for the team
3. Admin user clicks <b>Save</b> and sees a flash message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the subcategory and hidden label for the NFL category:**

![Admin user sees actions for the subcategory and hidden label for the NFL category](/sports_hub_portal/desktop_application_features/maintain_navigation/images/ia_subcategory_actions.png)

**2. Admin user sees actions for the team:**

![Admin user sees actions for the team](/sports_hub_portal/desktop_application_features/maintain_navigation/images/ia_team_actions.png)

**3. Admin user clicks Save and sees a flash message:**

![Admin user clicks Save and sees a flash message](/sports_hub_portal/desktop_application_features/maintain_navigation/images/ia_success_save.png)

</details>

## Test cases

1. Verify the ability to hide the category
2. Verify the ability to show the category
3. Verify the ability to hide the subcategory
4. Verify the ability to show the subcategory
5. Verify the ability to hide the team
6. Verify the ability to show the team

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the ability to hide the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) On the right of the visible category, click the ellipsis (...) button</br>2) Click <b>Hide</b>|2) The <b>Hidden</b> label is shown for the category. The category is not visible for users|

### **#2. Verify the ability to show the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the hidden category|1) On the right of the hidden category, click the ellipsis (...) button</br>2) Click <b>Show</b>|2) The <b>Hidden</b> label is not shown for the category. Category with all subcategories and teams is visible for users|

### **#3. Verify the ability to hide the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the visible subcategory|1) On the right of the visible subcategory, click the ellipsis (...) button</br>2) Click <b>Hide</b>|2) The <b>Hidden</b> label is shown for the subcategory. The subcategory is not visible for users|

### **#4. Verify the ability to show the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the hidden subcategory|1) On the right of the hidden subcategory, click the ellipsis (...) button</br>2) Click <b>Show</b>|2) The <b>Hidden</b> label is not shown for the subcategory. Subcategory with all teams is visible for users|

### **#5. Verify the ability to hide the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the visible team|1) On the right of the visible team, click the ellipsis (...) button</br>2) Click <b>Hide</b>|2) The <b>Hidden</b> label is shown for the team. The team is not visible for users|

### **#6. Verify the ability to show the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is the hidden team|1) On the right of the hidden team, click the ellipsis (...) button</br>2) Click <b>Show</b>|2) The <b>Hidden</b> label is not shown for the team. The team is visible for users|

</details>
