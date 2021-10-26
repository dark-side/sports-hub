### Back to [Page layout](../../) feature

# Page structure

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
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
Then I see the page consisting of:
  - Header section that is common for all pages includes:
    1. Main menu
    2. Sports Hub logo
    3. Profile menu
  - The main content area with content blocks, configured by admin
  - Footer section that is common to all pages, configured the admin

When I tap the Sports Hub logo
Then I am taken to the Sports Hub Home page
</pre>

## Mockups

1. Users see the navigation menu
2. Full Home page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the navigation menu:**

![Users see Home in the navigation menu](/sports_hub_portal/mobile_application_features/project_layout/images/application_navigation_menu.png)

**2. Full Home page:**

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
