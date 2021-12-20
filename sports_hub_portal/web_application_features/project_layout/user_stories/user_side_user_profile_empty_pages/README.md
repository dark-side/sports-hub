### Back to [Page layout on the portal](../../) feature

# Page structure (user side): user profile pages (user logged-in)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view personal profile pages when I am logged-in

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views profile section </i></b>

Given I am logged-in user

When I view any page on the site
Then I see the user profile in the Header section that contains:
  - User photo
  - User Name
  - Profile arrow to a drop-down

When I click on a Profile drop-down
The I see a popup with the following elements:
  - User name and email
  - <b>View profile</b> menu item
  - <b>Change password</b> menu item
  - <b>My surveys</b> menu item
  - <b>Team hub</b> menu item
  - <b>Log out</b>

When I click <b>View profile</b>
Then I am regirected to the empty profile page
  And <b>Personal</b> tab is active

When I click <b>Change password</b>
Then I am regirected to the empty profile page
  And <b>Change password</b> tab is active

When I click <b>My surveys</b>
Then I am regirected to the empty profile page
  And <b>My surveys</b> tab is active

When I click <b>Team hub</b>
Then I am regirected to the empty profile page
  And <b>Team hub</b> tab is active
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. User side mockup
2. Users see profile popup
3. Users see profile pages
4. Users see <b>Home</b> page structure when they are signed in
5. Users see <b>Home</b> page structure when they are not signed in

<details>
  <summary>Click here to see mockups details</summary>

**1. User side mockup:**

![User side mockup](/sports_hub_portal/web_application_features/project_layout/images/user_side_mockup.png)

**2. Users see profile popup:**

![Users see profile popup](/sports_hub_portal/web_application_features/project_layout/images/user_side_profile_popup.png)

**3. Users see profile pages:**

![Users see profile pages](/sports_hub_portal/web_application_features/project_layout/images/user_side_profile_pages.png)

**4. Users see Home page structure when they are signed in:**

![Users see Home page structure when they are signed in](/sports_hub_portal/web_application_features/project_layout/images/home_page_logged_in_user.png)

**5. Users see Home page structure when they are not signed in:**

![Users see Home page structure when they are not signed in](/sports_hub_portal/web_application_features/project_layout/images/home_page_logged_out_user.png)

</details>

## Test cases

1. Verify that the user profile pages correspond to the mockup

<details>
  <summary>Click here to see test cases details</summary>

### **1. Verify that the user profile pages correspond to the mockup:**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Log in with user account|1) View that the user profile pages correspond to the mockup|
</details>
