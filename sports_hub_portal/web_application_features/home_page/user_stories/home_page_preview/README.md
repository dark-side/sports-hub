### Back to [Home page of the portal](../../README.md) feature

# Allow admin user to preview the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to preview the Home page while configuration
    So that I could review the page as a site user

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user previews the Home page</i></b>

Given I am logged in as an admin user

When I am on the <b>Home</b> configuration page
Then I see the <b>Preview</b> button

When I click the <b>Preview</b> button
Then I see the <b>Home</b> page in regular user mode
  And I see the <b>Back to edit page</b> button

When I click the <b>Back to edit page</b> button
Then I am taken back to the <b>Home</b> configuration page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Home</b> configuration page
2. Admin user sees the <b>Home</b> preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Home configuration page:**

![Admin user sees the Home configuration page](/sports_hub_portal/web_application_features/home_page/images/home_configuration.png)

**2. Admin user sees the Home preview page:**

![Admin user sees the Home preview page](/sports_hub_portal/web_application_features/home_page/images/home_preview_page.png)

</details>

## Test cases

1. Verify that admin is able to preview the <b>Home</b> page and navigate back to the configuration page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to preview the Home page and navigate back to the configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Home</b> configuration page</br>- Update the <b>Main articles</b> section</br>- Update the <b>Breakdown</b> section</br>- Update the <b>Photo of the day</b> section|1) Click <b>Preview</b></br>2) Click <b>Back to edit page</b>|1) The <b>Home</b> page is shown for admin as it will be shown for the users</br>2) Admin navigates back to the <b>Home</b> configuration page|

</details>
