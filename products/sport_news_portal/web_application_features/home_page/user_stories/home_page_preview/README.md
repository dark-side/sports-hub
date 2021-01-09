### Back to [Home page of the portal](../../) feature

# Allow admin user to preview the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to preview Home page while configuration
    So that I could review the page as a site user

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user previews the Home page</i></b>

Given I am logged in as an admin user

When I am on the <b>Home</b> configuration page
Then I see the <b>Preview</b> button

When I click the <b>Preview</b> button
Then I see a home page in regular user mode
  And I see <b>Back to edit page</b> button

When I click the <b>Back to edit page</b> button
Then I am taken back to the <b>Home</b> configuration page
</pre>

## Mockups

1. Admin user sees a Home configuration page
2. Admin user sees a Home preview page

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a Home configuration page:**

![Admin user sees a Home configuration page](/products/sport_news_portal/web_application_features/home_page/images/home_configuration.png)

**2. Admin user sees a Home preview page:**

![Admin user sees a Home preview page](/products/sport_news_portal/web_application_features/home_page/images/home_preview_page.png)

</details>

## Test cases

1. Verify that admin is able to preview the home page and navigate back to the configuration page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to preview the home page and navigate back to the configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Home</b> configuration page</br>- Update <b>Main articles</b> section</br>- Update <b>Breakdown</b> section</br>- Update <b>Photo of the day</b> section|1) Click <b>Preview</b> button</br>2) Click <b>Back to edit page</b> button|1) The <b>Home</b> page is shown for admin as it will be shown for the users</br>2) Admin navigates back to the <b>Home</b> configuration page|

</details>
