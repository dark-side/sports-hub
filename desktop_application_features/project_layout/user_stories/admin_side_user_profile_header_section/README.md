### Back to [Page layout on the portal](../../README.md) feature

# Page structure (admin side): user profile section in the header

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to see my name when I am logged-in

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the user profile section in the administration office</i></b>

Given I am logged in as an admin user

When I view the administration office
Then I see the user profile in the Header section that contains:
  - User photo
  - User Name
  - <b>Administrator</b> hint text
  - Profile arrow to a drop-down

When I click on a Profile drop-down
The I see a popup with the following elements:
  - User name and email
  - Log out

When I hover over the menu items in the popup
Then I see the colour of that item is changed
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Administration side mockup
2. Admin user sees administration side
3. Admin user sees a profile popup
4. Admin user hovers over the <b>Log out</b> button

<details>
  <summary>Click here to see mockups details</summary>

**1. Administration side mockup:**

![Admin user sees administration side](/desktop_application_features/project_layout/images/admin_mockup.png)

**2. Admin user sees administration side:**

![Admin user sees administration side](/desktop_application_features/project_layout/images/admin_side.png)

**3. Admin user sees a profile popup:**

![Admin user sees a profile popup](/desktop_application_features/project_layout/images/admin_profile.png)

**4. Admin user hovers over the Log outbutton:**

![Admin user hovers over the Log outbutton](/desktop_application_features/project_layout/images/admin_log_out_hover.png)

</details>

## Test cases

1. Verify that the user profile section corresponds to the mockup

<details>
  <summary>Click here to see test cases details</summary>

### **1. Verify that the user profile section corresponds to the mockup:**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Log in with admin account|1) View that the user profile section corresponds to the mockup|
</details>
