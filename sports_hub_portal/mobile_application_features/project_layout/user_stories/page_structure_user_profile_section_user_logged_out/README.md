### Back to [Page layout in the application](../../README.md) feature

# Page structure: user profile section in the header (user logged out)

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to see Sign up and Log in links when I am logged out

## Acceptance criteria

<pre>
<b><i>Scenario: A user views layout structure across all the pages</i></b>

Given I am a user

When I view any page
Then I see the user profile icon (or the user photo if added) in the Header section

When I tap a Profile icon
The I see a popup with the following elements:
  - <b>Sign up</b>
  - <b>Log in</b>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a profile icon in the Header section
2. Users see a popup after they tap the profile icon

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a profile icon in the Header section:**

![Users see a profile icon in the Header section](/sports_hub_portal/mobile_application_features/project_layout/images/profile_icon_home_page.png)

**2. Users see a popup after they tap the profile icon:**

![Users see a popup after they tap the profile icon](/sports_hub_portal/mobile_application_features/project_layout/images/profile_popup_home_page_logged_out.png)

</details>

## Test cases

1. Verify that the logged out user sees a profile icon and profile popup

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the logged out user sees a profile icon and profile popup**

|Preconditions|Steps|Expected result
------|-------|----------
|- Go to the Sports Hub Home page</br>- The user is logged out|1) Go to any page</br>2) Observe the header section</br>3) Tap the profile icon|2) The profile icon is present in the header section on the right</br>3) The profile popup appears with the following elements:</br>- Sign up</br>- Log in|
</details>
