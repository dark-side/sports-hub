### Back to [Surveys](../../) feature

# Allow users to see a list of all surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to see a list of all surveys
    So that I can vote

## Acceptance criteria

<pre>
<b><i>Scenario: A user visits My surveys page</i></b>

Given I am logged in as a user

When I view any page of the application
  And I tap the my profile picture at the top of the page
Then I see the <b>My surveys</b> menu item

When I tap <b>My surveys</b>
Then I see the <b>My surveys</b> page is opened
  And I see the system displays only surveys published by admin
  And I see the system displays two tabs: <b>Opened</b> and <b>Closed</b>
  And I see the <b>Opened</b> tab is active by default

When I tap <b>Opened</b>
Then I see the <b>Opened</b> list contains active surveys and is sorted by creation date
  And I see each survey can be expanded by the Expand icon
  And I see each survey has Due date
  And I see <b>Sort by</b> dropdown with Newest (default), Most Popular and About to Expire options

When I tap <b>Closed</b>
Then I see the <b>Closed</b> list contains closed surveys and is sorted by close date
  And I see each survey can be expanded by the Expand icon
  And I see each survey has Close date
  And I see the filter there with All surveys, Voted options (NOTE: <i>Voted</i> surveys are surveys user participated in)
</pre>

## Mockups

1. Logged-in with email users see <b>My surveys</b> in the profile menu
2. Logged-in with a third party users see <b>My surveys</b> in the profile menu
3. Users see the <b>Opened</b> tab on the <b>My surveys</b> page
4. Users see the <b>Closed</b> tab on the <b>My surveys</b> page
5. Users see <b>Sort by</b> options on the <b>Opened</b> tab
6. Users see filter options on the <b>Closed</b> tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Logged-in with email users see My surveys in the profile menu:**

![Logged-in with email users see My surveys in the profile menu](/products/sports_hub_portal/mobile_application_features/surveys/images/application_user_profile_menu_logged_with_email.png)

**2. Logged-in with a third party users see My surveys in the profile menu:**

![Logged-in with a third party users see My surveys in the profile menu](/products/sports_hub_portal/mobile_application_features/surveys/images/application_user_profile_menu_logged_with_third_party.png)

**3. Users see the Opened tab on the My surveys page:**

![Users see the Opened tab on the My surveys page](/products/sports_hub_portal/mobile_application_features/surveys/images/application_opened_surveys.png)

**4. Users see the Closed tab on the My surveys page:**

![Users see the Closed tab on the My surveys page](/products/sports_hub_portal/mobile_application_features/surveys/images/application_closed_surveys.png)

**5. Users see Sort by options on the Opened tab:**

![Users see Sort by options on the Opened tab](/products/sports_hub_portal/mobile_application_features/surveys/images/application_sort_by_opened_surveys.png)

**6. Users see filter options on the Closed tab:**

![Users see filter options on the Closed tab](/products/sports_hub_portal/mobile_application_features/surveys/images/application_filter_closed_surveys.png)

</details>

## Test cases

1. Verify the content of the <b>Opened</b> tab on the <b>My surveys</b> page
2. Verify that users can sort surveys by <b>Newest</b>, <b>Most Popular</b>, <b>About to Expire</b> on the <b>Opened</b> tab on the <b>My surveys</b> page
3. Verify the content of the <b>Closed</b> tab on the <b>My surveys</b> page
4. Verify that users can filter surveys by <b>Voted</b>, <b>All surveys</b> on the <b>Closed</b> tab on the <b>My surveys</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Opened tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) Tap the profile picture</br>2) Tap the <b>My surveys</b> item</br>3) Examine the <b>Opened</b> tab|2) The <b>My surveys</b> page is opened</br>3) The <b>Opened</b> tab is opened by default. The <b>Opened</b> tab contains all active surveys. Each survey has the Expand icon. Each survey has Due date shown. Surveys are sorted from the newest to oldest|

### **#2. Verify that users can sort surveys by Newest, Most Popular, About to Expire on the Opened tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab|1) Select <b>Sort by link</b></br>2) Tap <b>Most Popular</b></br>3) Select <b>Sort by</b> link</br>4) Tap A<b>bout to Expire</b></br>5) Select <b>Sort by</b> link</br>6) Tap <b>Newest</b>|2) Surveys are sorted according to the amount of users voted from the biggest number</br>4) Surveys are sorted according to the end date from the closest one</br>6) Surveys are sorted according to the date of creation from the newest one|

### **#3. Verify the content of the Closed tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) Tap the user’s profile picture</br>2) Tap <b>My surveys</b> item</br>3) Select <b>Closed</b> tab</br>4) Examine the <b>Closed</b> tab|2) The <b>My surveys</b> page is opened</br>3) The <b>Closed</b> tab is opened</br>4) The <b>Closed</b> tab contains all closed surveys. Each survey has the Expand icon. Each survey has a Close date shown. Surveys are sorted from the newest to oldest by close date|

### **#4. Verify that users can filter surveys by Voted, All surveys on the Closed tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Closed</b> tab|1) Tap <b>Filter</b> icon</br>2) Tap <b>Voted</b></br>3) Tap <b>Filter</b> icon</br>4) Tap <b>All surveys</b>|2) All surveys the user has participated in are shown</br>4) All surveys are shown|

</details>
