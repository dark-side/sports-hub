### Back to [Page layout on the portal](../../README.md) feature

# Page structure (admin side): header section

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the header section

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the administration office</i></b>

Given I am logged in as an admin user

When I view the administration office
Then I see the header section includes:
  1. Sports Hub logo
  2. Empty section for a switch button
  3. Empty section for user profile details
  4. Horizontal section for active configuration page name
  5. Horizontal menu with static page links: Home (active by default), Lifestyle, Video, Dealbook)
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Administration side mockup
2. Admin user sees administration side

<details>
  <summary>Click here to see mockups details</summary>

**1. Administration side mockup:**

![Admin user sees administration side](/desktop_application_features/project_layout/images/admin_mockup.png)

**2. Admin user sees administration side:**

![Admin user sees administration side](/desktop_application_features/project_layout/images/admin_side.png)

</details>

## Test cases

1. Verify that the header section corresponds to the mockup

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to act as a user by clicking Switch to user view**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Log in with admin account|1) View that the header corresponds to the mockup|
</details>
