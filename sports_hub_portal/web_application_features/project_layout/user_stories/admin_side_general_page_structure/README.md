### Back to [Page layout on the portal](../../README.md) feature

# Page structure (admin side): general sections

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the same layout structure across all the pages

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the administration office</i></b>

Given I am logged in as an admin user

When I view the administration office
Then I see the page layout has the following EMPTY sections:
  - Header section
  - Left vertical menu
  - The main admin work area
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Administration side mockup
2. Admin user sees administration side

<details>
  <summary>Click here to see mockups details</summary>

**1. Administration side mockup:**

![Admin user sees administration side](/sports_hub_portal/web_application_features/project_layout/images/admin_mockup.png)

**2. Admin user sees administration side:**

![Admin user sees administration side](/sports_hub_portal/web_application_features/project_layout/images/admin_side.png)

</details>

## Test cases

1. Verify that the page layout corresponds to the style guides

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the page layout corresponds to the style guides**

|Preconditions|Steps|Expected result
------|-------|----------
|- Log in with admin account|1) View the page</br>|2) The page structure corresponds to the style guides|

</details>
