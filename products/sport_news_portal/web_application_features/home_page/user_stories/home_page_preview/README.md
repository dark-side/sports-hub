### Back to [Home page of the portal](../../) feature

# Allow admin user to preview the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to preview Home page while configuration
    So that I could review the page as user

## Acceptance criteria

    Scenario: An admin user previews Home page
    Given I am logged in as an admin user

    When I am on Home configuration page
    Then I see a Preview icon
    When I click on that icon
    Then I see a Home page as for site users
    When I click on that icon again
    Then I am taken back to the Home configuration page

## Mockups

1. The admin user sees configured Home Page
2. The admin user preview the Home Page

<details>
  <summary>Click here to see mockups details</summary>

**1. The admin user sees configured Home Page:**

![Home Page](/products/sport_news_portal/web_application_features/home_page/images/home_page_admin_side.png)

**2. The admin user preview the Home Page:**

![Home Page](/products/sport_news_portal/web_application_features/home_page/images/preview_home_page.png)

</details>

## Test Scenarios

1. Verify clicking on Preview icon

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify clicking on Preview icon**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Click on preview icon|Then the system is displayed the Home page as for site users
|4|Click on preview icon again|Admin navigates back to the Home configuration page
</details>
