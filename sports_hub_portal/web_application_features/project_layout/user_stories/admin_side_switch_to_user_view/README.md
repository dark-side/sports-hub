### Back to [Page layout on the portal](../../) feature

# Page structure (admin side): switch to user view

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to swith to a user view

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user switches between admin and user views</i></b>

Given I am logged in as an admin user

When I view the administration office
Then I see <b>Switch to user view</b> button in the header section

When I hover over <b>Switch to user view</b> button
Then I see it's name

When I click the <b>Switch to user view</b> button
Then button changes to the <b>Switch to admin view</b>
  And I am taken to the user side of Sports Hub home page where I can act as a regular user

When I click the <b>Switch to admin view</b> button
Then button changes to the <b>Switch to user view</b>
  And I am taken to the admin side of Sports Hub home page where I can act as an admin
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Administration side mockup
2. Admin user hovers over the <b>Switch to user view</b>
3. Admin user hovers over the <b>Switch to admin view</b>
4. Admin user sees administration side

<details>
  <summary>Click here to see mockups details</summary>

**1. Administration side mockup:**

![Admin user sees administration side](/sports_hub_portal/web_application_features/project_layout/images/admin_mockup.png)

**2. Admin user hovers over the Switch to user view:**

![Admin user hovers over the Switch to user view](/sports_hub_portal/web_application_features/project_layout/images/admin_side_switch_to_user.png)

**3. Admin user hovers over the Switch to admin view:**

![Admin user hovers over the Switch to admin view](/sports_hub_portal/web_application_features/project_layout/images/user_side_switch_to_admin.png)

**4. Admin user sees administration side:**

![Admin user sees administration side](/sports_hub_portal/web_application_features/project_layout/images/admin_side.png)

</details>

## Test cases

1. Verify that admin is able to act as a user by clicking <b>Switch to user view</b>
2. Verify that admin is able to go back to admin view by clicking <b>Switch to admin view</b>

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to act as a user by clicking Switch to user view**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Log in with admin account|1) Go to any page</br>2) Click **Switch to user view** in the upper-right corner of the page</br>3) Browse different pages|2) Admin goes to the home page in the user view mode</br>3) Admin can interact with pages as a regular user|

### **#2. Verify that admin is able to go back to admin view by clicking Switch to admin view**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Log in with admin account</br>- Admin in the user view mode|1) Go to any page</br>2) Click **Switch to admin view** in the upper-right corner of the page</br>3) Browse different pages|2) Admin goes to the home page in admin mode</br>3) Admin can interact with pages as an admin|

</details>
