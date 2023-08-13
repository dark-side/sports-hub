### Back to [Page layout on the portal](../../README.md) feature

# Page structure (user side): general sections

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view the same layout structure across all the pages

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views layout structure across all the pages</i></b>

Given I am a site user

When I view any page on the site
Then I see the page layout has the following EMPTY sections for:
  - Header section with the empty blocks for:
    - Search
    - Social media
    - Profile
    - Languages
  - The main content area
  - Left sidebar
  - Right sidebar
  - Footer section
  And I see the <b>Sports Hub</b> logo

When I click the <b>Sports Hub</b> logo
Then I am taken to the Sports Hub home page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. User side mockup
2. Users see <b>Home</b> page structure when they are signed in
3. Users see <b>Home</b> page structure when they are not signed in

<details>
  <summary>Click here to see mockups details</summary>

**1. User side mockup:**

![User side mockup](/sports_hub_portal/web_application_features/project_layout/images/user_side_mockup.png)

**2. Users see Home page structure when they are signed in:**

![Users see Home page structure when they are signed in](/sports_hub_portal/web_application_features/project_layout/images/home_page_logged_in_user.png)

**3. Users see Home page structure when they are not signed in:**

![Users see Home page structure when they are not signed in](/sports_hub_portal/web_application_features/project_layout/images/home_page_logged_out_user.png)

</details>

## Test cases

1. Verify that the page layout corresponds to the mockup
2. Verify that the user is able to navigate to the <b>Home</b> page by selecting the logo

<details>
  <summary>Click here to see test cases details</summary>


### **#1. Verify that the page layout corresponds to the mockup**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Log in with user account|1) View that the page layout corresponds to the mockup|

### **#2. Verify that the user is able to navigate to the Home page by selecting the logo**

|Preconditions|Steps|Expected result
------|-------|----------
|Go to the Sports Hub home page|1) Go to any page</br>2) In the upper-left corner of the page, select the logo|2) The user goes to the home page|

</details>
