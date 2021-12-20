### Back to [Page layout on the portal](../../) feature

# Page structure (admin side): left vertical menu

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to view the left vertical menu (local navigation)

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the left vertical menu</i></b>

Given I am logged in as an admin user

When I view the administration office
Then I see the left vertical menu with the following items:
  1. Surveys
  2. Banners
  3. Languages
  4. Footer
  5. Social Networks
  6. Users
  7. Information architecture
  8. Teams
  9. News Partners
  10. Advertising

When I hover over items on the left vertical menu
Then I see their names
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Administration side mockup
2. Admin user sees administration side
3. Admin user hovers over the Surveys menu item

<details>
  <summary>Click here to see mockups details</summary>

**1. Administration side mockup:**

![Admin user sees administration side](/sports_hub_portal/web_application_features/project_layout/images/admin_mockup.png)

**2. Admin user sees administration side:**

![Admin user sees administration side](/sports_hub_portal/web_application_features/project_layout/images/admin_side.png)

**3. Admin user hovers over the Surveys menu item:**

![Admin user hovers over the Surveys menu item](/sports_hub_portal/web_application_features/project_layout/images/admin_side_left_menu_item_hover.png)

</details>

## Test cases

1. Verify that the left vertical menu corresponds to the mockup and item names appear on the hover

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the left vertical menu corresponds to the mockup and item names appear on the hover**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page</br>- Log in with admin account|1) Go to any page</br>2) Hover over any menu item|1) View that the left vertical menu corresponds to the mockup</br>2) Admin sees an item name|
</details>
