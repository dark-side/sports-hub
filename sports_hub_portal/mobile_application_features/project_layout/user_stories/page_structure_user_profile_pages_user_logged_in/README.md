### Back to [Page layout in the application](../../) feature

# Page structure: user profile pages (user logged-in)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view personal profile pages when I am logged-in

## Acceptance criteria

<pre>
<b><i>Scenario: A user views layout structure across all the pages</i></b>

Given I am logged-in user

When I view any page and tap the profile icon
Then I see a popup

When I tap <b>Personal</b>
Then I am regirected to the empty profile page

When I tap <b>Change password</b>
Then I am regirected to the empty <b>Change password</b> page

When I tap <b>My surveys</b>
Then I am regirected to the empty <b>My surveys</b> page

When I tap <b>Team hub</b>
Then I am regirected to the empty <b>Team hub</b> page

<i>Note: implement redirect to these empty pages</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a popup after they tap the profile icon
2. Users see a <b>Personal</b> page
3. Users see a <b>Change password</b> page
4. Users see a <b>My surveys</b> page
5. Users see a <b>Team hub</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a popup after they tap the profile icon:**

![Users see a popup after they tap the profile icon](/sports_hub_portal/mobile_application_features/project_layout/images/profile_popup_home_page.png)

**2. Users see a Personal page:**

![Users see a Personal page](/sports_hub_portal/mobile_application_features/project_layout/images/personal_page.png)

**3. Users see a Change password page:**

![Users see a Change password page](/sports_hub_portal/mobile_application_features/project_layout/images/change_password_page.png)

**4. Users see a My surveys page:**

![Users see a My surveys page](/sports_hub_portal/mobile_application_features/project_layout/images/my_surveys_page.png)

**5. Users see a Team hub page:**

![Users see a Team hub page](/sports_hub_portal/mobile_application_features/project_layout/images/team_hub_page.png)

</details>

## Test cases

1. Verify that user is redirected to a <b>Personal</b> page from a profile popup
2. Verify that user is redirected to a <b>Change password</b> page from a profile popup
3. Verify that user is redirected to a <b>My surveys</b> page from a profile popup
4. Verify that user is redirected to a <b>Team hub</b> page from a profile popup

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that user is redirected to a Personal page from a profile popup**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub Home page|1) Tap the profile icon in header</br>2) Tap the <b>Personal</b> menu item|2) The user is redirected to the <b>Personal</b> page|

### **#2. Verify that user is redirected to a Change password page from a profile popup**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub Home page|1) Tap the profile icon in header</br>2) Tap the <b>Change password</b> menu item|2) The user is redirected to the <b>Change password</b> page|

### **#3. Verify that user is redirected to a My surveys page from a profile popup**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub Home page|1) Tap the profile icon in header</br>2) Tap the <b>My surveys</b> menu item|2) The user is redirected to the <b>My surveys</b> page|

### **#4. Verify that user is redirected to a Team hub page from a profile popup**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub Home page|1) Tap the profile icon in header</br>2) Tap the <b>Team hub</b> menu item|2) The user is redirected to the <b>Team hub</b> page|
</details>
