### Back to [Maintain navigation on the portal](../../) feature

# Allow admin users to show and hide navigation menu items on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to show and hide the navigation menu categories, subcategories, and teams on the portal

## Acceptance criteria

<pre>
Scenario: An admin user show/hides the navigation menu categories, subcategories, and teams
Given I am logged in as an admin user

When I am on the <b>Information architecture</b> configuration page
Then I see the list of navigation menu categories and the <b>Save</b> button

When I hover over a category, subcategory, or team name
Then on the right of each category/subcategory/team name, I see the ellipsis (...) button

When I click the ellipsis (...) button for any created category
Then I see options to <b>Delete</b>, <b>Edit</b>, and <b>Hide</b> (<b>Show</b>) category

When I click the ellipsis (...) button for any created subcategory/team
Then I see options to <b>Delete</b>, <b>Edit</b>, <b>Hide</b> (<b>Show</b>), <b>Move</b> subcategory/team

When I click the ellipsis (...) button for static categories (<b>Lifestyle</b>, <b>Dealbook</b>, <b>Video</b>, <b>Team hub</b>)
Then I see an option to <b>Hide</b> category

When I click to <b>Hide</b> not hidden category/subcategory/team
Then I see selected category/subcategory/team is not displayed on the users UI
  And the "Hidden" label is shown for that category/subcategory/team on the <b>Information architecture</b> configuration page

When I click to <b>Show</b> a hidden category/subcategory/team
Then I see the selected category/subcategory/team is displayed on the users UI
  And the "Hidden" label is not shown anymore for that appropriate category/subcategory/team on the <b>Information architecture</b> configuration page

When I click <b>Save</b> at the top of the page
Then I see changes applied to the category/subcategory/team are saved
</pre>

## Mockups

1. Admin user sees actions for the subcategory and hidden label for the NFL category
2. Admin user sees actions for the team
3. Admin user clicked Save and sees a flash message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for the subcategory and hidden label for the NFL category:**

![Admin user sees actions for the subcategory and hidden label for the NFL category](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_subcategory_actions.png)

**2. Admin user sees actions for the team:**

![Admin user sees actions for the team](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_team_actions.png)

**3. Admin user clicked Save and sees a flash message:**

![Admin user clicked Save and sees a flash message](/products/sport_news_portal/web_application_features/maintain_navigation/images/ia_success_save.png)

</details>

## Test cases

1. Verify the ability to hide the category
2. Verify the ability to unhide the category
3. Verify the ability to hide the subcategory
4. Verify the ability to unhide the subcategory
5. Verify the ability to hide the team
6. Verify the ability to unhide the team

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the ability to hide the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Information Architecture</b> configuration page|1) On the right of an unhidden category, click the ellipsis (...) button</br>2) Click <b>Hide</b>|2) The <b>Hidden</b> label is shown for the category. The category is not visible for users|

### **#2. Verify the ability to unhide the category**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is a hidden category|1) On the right of a hidden category, click the ellipsis (...) button</br>2) Click <b>Show</b>|2) The <b>Hidden</b> label is not shown for the category. Category with all subcategories and teams is visible for users|

### **#3. Verify the ability to hide the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is an unhidden subcategory|1) On the right of an unhidden subcategory, click the ellipsis (...) button</br>2) Click <b>Hide</b>|2) The <b>Hidden</b> label is shown for the subcategory. The subcategory is not visible for users|

### **#4. Verify the ability to unhide the subcategory**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is a hidden subcategory|1) On the right of a hidden subcategory, click the ellipsis (...) button</br>2) Click <b>Show</b>|2) The <b>Hidden</b> label is not shown for the subcategory. Subcategory with all teams is visible for users|

### **#5. Verify the ability to hide the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is an unhidden team|1) On the right of an unhidden team, click the ellipsis (...) button</br>2) Click <b>Hide</b>|2) The <b>Hidden</b> label is shown for the team. The team is not visible for users|

### **#6. Verify the ability to unhide the team**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Information Architecture</b> configuration page</br>- There is a hidden team|1) On the right of a hidden team, click the ellipsis (...) button</br>2) Click <b>Show</b>|2) The <b>Hidden</b> label is not shown for the team. The team is visible for users|

</details>
