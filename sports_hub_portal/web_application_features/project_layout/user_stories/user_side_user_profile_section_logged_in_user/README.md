### Back to [Page layout on the portal](../../README.md) feature

# Page structure (user side): user profile section in the header (user logged-in)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see my name when I am logged-in

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views profile section when they are logged-in</i></b>

Given I am logged-in user

When I view any page on the site
Then I see the user profile in the Header section that contains:
  - User photo
  - User Name
  - Profile arrow to a drop-down

When I click on a Profile arrow
The I see a popup with the following elements:
  - User name and email
  - View profile menu item
  - Change password menu item
  - My surveys menu item
  - Team hub menu item
  - Log out

When I hover over the menu items in the popup
Then I see the colour of that item is changed
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see <b>Home</b> page structure when they are signed in
2. Users see profile popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see Home page structure when they are signed in:**

![Users see Home page structure when they are signed in](/sports_hub_portal/web_application_features/project_layout/images/home_page_logged_in_user.png)

**2. Users see profile popup:**

![Users see profile popup](/sports_hub_portal/web_application_features/project_layout/images/user_side_profile_popup.png)

</details>

## Test cases

1. Verify that the user sees their name, photo, and profile popup

<details>
  <summary>Click here to see test cases details</summary>

### **1. Verify that the user sees their name, photo, and profile popup:**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub home page|1) Log in with user account</br>2) View that the user profile section</br>3) Click the profile arrow>|2) See user name, photo, profile arrow</br>3) See user name, email, and the menu|
</details>
