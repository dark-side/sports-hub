### Back to [Banners on the portal](/../../) feature

# Allow users to view banner on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to view banners at the right sidebar of the site 
    So that I can see reminders about upcoming sport events, important updates, etc


## Acceptance criteria

    Scenario: A site user views banners at the right sidebar of the site
    Given I am logged in as a site user

    When I view a page within the category that has some banner(s) published
    Then I see a banner(s) photo in the right sidebar

## Mockups

1. User sees banner at the right sidebar of the site

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees banner at the right sidebar of the site:**

![Article Screen](/products/sport_news_portal/web_application_features/banners/images/banner_at_the_home_page.png)


</details>

## Test Scenarios

1. Verify that user is able to view banners if they are published

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that user is able to view banners if they are published**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|User is navigated to the home page
|3|Observe the right sidebar| There are banner(s) photo in the right sidebar

</details>
