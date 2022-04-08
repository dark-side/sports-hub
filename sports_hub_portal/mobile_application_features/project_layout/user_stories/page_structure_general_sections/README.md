### Back to [Page layout in the application](../../) feature

# Page structure: general sections

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view the same layout structure across all the pages

## Acceptance criteria

<pre>
<b><i>Scenario: A user views layout structure across all the pages</i></b>

Given I am a user

When I view any page
Then I see the page layout has the following EMPTY sections for:
  - Header section with the empty blocks for:
    - Main menu icon
    - Sports Hub logo
    - Profile icon
    - Search
  - The main content area with content blocks, configured by admin
  - Footer section that is common to all pages, configured the admin

When I tap the Sports Hub logo
Then I am taken to the Sports Hub Home page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Full Home page

<details>
  <summary>Click here to see mockups details</summary>

**1. Full Home page:**

![Full Home page](/sports_hub_portal/mobile_application_features/project_layout/images/home_page.png)

</details>

## Test cases

1. Verify that users are able to navigate to the Home page by tapping the logo

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users are able to navigate to the Home page by tapping the logo**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub Home page|1) Go to any page</br>2) Tap the logo in header|2) The user is redirected to the Home page|

</details>
