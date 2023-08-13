### Back to [Banners on the portal](../../README.md) feature

# Allow admin users to configure predefined banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure predefined banners on the portal

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures the list of predefined banners</i></b>

Given I am logged in as an admin user

When I view the <b>Banners</b> configuration page
Then I see the <b>Predefined Banners</b> section below the configurable banners section with the following:
  - <b>Facebook Video</b>, <b>Facebook Post</b>, <b>Lifestyle</b>, <b>Dealbook</b> list of predefined banners
  - <b>Show/Hide</b> toggle for each specific predefined banner (<b>Show</b> is on by default)

When I click the <b>Show</b> toggle for any of the predefined banner from the list
Then the toggle changes to <b>Hide</b>

When I click the <b>Hide</b> toggle for any of the predefined banners from the list
Then the toggle changes to <b>Show</b>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>Opened</b> and <b>Predefined banners</b> tabs on the <b>Banners</b> configuration page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Opened and Predefined banners tabs on the Banners configuration page:**

![Admin user sees Opened and Predefined banners tabs on the Banners configuration page](/web_application_features/banners/images/banners_open_tab.png)

</details>

## Test cases

1. Verify that admin can hide the predefined banner by the <b>Show</b> toggle
2. Verify that admin can unhide the predefined banner by the <b>Hide</b> toggle

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can hide the predefined banner by the Show toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page|1) Click the <b>Show</b> toggle to hide any predefined banner from the list</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if the hidden predefined banner is not visible to the site user|1) The toggle changes to <b>Hide</b></br>4) The hidden predefined banner is not shown|

### **#2. Verify that admin can unhide the predefined banner by the Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Banners</b> configuration page</br>- Some predefined banners are hidden|1) Click the <b>Hide</b> toggle to hide any predefined banner from the list</br>2) Log out of admin account</br>3) Log in with user account</br>4) Check if the hidden predefined banner is not visible to the site user|1) The toggle changes to <b>Show</b></br>4) The unhidden predefined banner is shown|

</details>
