### Back to [Manage Advertisements on the portal](/../../) feature

# Allow users to see Advertisements

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to view advertisement at the top of the right sidebar of the site


## Acceptance criteria

    Scenario: A site user views advertisement at the top of the right sidebar
    Given I am logged in as a site user

    When I view a page of the Sport News and the advertisements are configured to be shown on the CMS
    Then I see an advertisement in the top right of the right sidebar
    When I view the advertisement is site-wide 
    Then I see it in any page of the site
    When I view the advertisement is category-related
    Then I see it only when I view page related to the specified advertisement category

## Mockups

1. User views Ads 

<details>
  <summary>Click here to see mockups details</summary>

**1. User views Ads:**

![View Ads Screen](/products/sport_news_portal/web_application_features/manage_ads/images/display_ads.png)

</details>

## Test Scenarios

1. Verify that user is able to view ads at the right sidebar
2. Verify that user is able to view site-wide ads on any page
3. Verify that user is able to view category-related Ads only on specific page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that user is able to view ads at the right sidebar**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Observe Ads on Home page|Logged in user is able to view ads at the right sidebar

### **#2. Verify that user is able to view site-wide ads on any page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Observe Ads on Home page|Logged in user is able to view ads at the right sidebar in any page of the site

### **#3. Verify that user is able to view category-related Ads only on specific page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Navigate to NBA category|Logged in user can view category-related Ads on NBA page
|4|Navigate to another category|Logged in user can not view NBA related Ads on another category pages

</details>
