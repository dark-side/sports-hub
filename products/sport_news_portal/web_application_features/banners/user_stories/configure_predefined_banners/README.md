### Back to [Banners on the portal](../../) feature

# Allow admin users to configure predefined banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure predefined banners on the portal

## Acceptance criteria

<pre>
Scenario: An admin user configures the list of predefined banners
Given I am logged in as an admin user

When I view the <b>Banners</b> configuration page
Then I see the <b>Predefined Banners</b> section below the configurable banners section with the following:
  - <b>Facebook Video</b>, <b>Facebook Post</b>, <b>Lifestyle</b>, <b>Dealbook</b> list of predefined banners
  - <b>Show/Hide</b> toggle for each specific predefined banner (<b>Show</b> is on by default)

When I click the <b>Show</b> toggle for any of the predefined banner from the list
Then toggle changes to <b>Hide</b>

When I click <b>Hide</b> toggle for any of the predefined banners from the list
Then toggle changes to <b>Show</b>
</pre>

## Mockups

1. Admin user sees Open tab and Predefined Banners on the Banners configuration page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Open tab and Predefined Banners on the Banners configuration page:**

![Admin user sees Open tab and Predefined Banners on the Banners configuration page](/products/sport_news_portal/web_application_features/banners/images/banners_open_tab.png)

</details>

## Test cases

1. Verify that admin can hide predefined banner by Show toggle
2. Verify that admin can unhide predefined banner by Hide toggle

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can hide predefined banner by Show toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page|1) Click <b>Show</b> toggle to hide any predefined banner from the list</br>2) Log out by admin account</br>3) Log in by user account</br>4) Check if the hidden predefined banner is not visible for the site user|1) Toggle changed to <b>Hide</b></br>4) The hidden predefined banner is not shown|

### **#2. Verify that admin can unhide predefined banner by Hide toggle**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Banners</b> configuration page</br>- Some predefined banners are hidden|1) Click <b>Hide</b> toggle to hide any predefined banner from the list</br>2) Log out by admin account</br>3) Log in by user account</br>4) Check if the hidden predefined banner is not visible for the site user|1) Toggle changed to <b>Show</b></br>4) The unhidden predefined banner is shown|

</details>
