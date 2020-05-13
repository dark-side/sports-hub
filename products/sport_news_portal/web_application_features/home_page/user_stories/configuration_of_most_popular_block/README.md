### Back to [Home page of the portal](/../../) feature

# Allow admin user to configure Most Popular block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to show/hide Most Popular block from Home page

## Acceptance criteria

    Scenario: An admin user configures Most Popular block from Home page
    (most popular articles - most visited during last month)
    Given I am logged in as an admin user

    When I am on Home configuration page
    Then I see a Most Popular block and show/hide toggle after Photo of the Day block
    When I click show/hide and click Publish
    Then I see a Most Popular block is shown/hidden on the Home Page

## Mockups

1. The admin user sees Home Page 
2. The admin user sees configured Home Page

<details>
  <summary>Click here to see mockups details</summary>

**1. The admin user sees Home Page:**

![Home Page](/products/sport_news_portal/web_application_features/home_page/images/home_page_admin_side_empty.png)

**2. The admin user sees configured Home Page:**

![Home Page](/products/sport_news_portal/web_application_features/home_page/images/home_page_admin_side.png)

</details>

## Test Scenarios

1. Verify that Most Popular block contains required fields
2. Verify selecting Category in the Most Popular block
3. Verify selecting Conference in the Most Popular block

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that Most Popular block contains required fields**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Verify the Most Popular block fields|Most Popular block contains next fields:<br> - Category - contains a list of all sport categories<br> - Conference - contains a list of all conferences<br> - Team - contains a list of all teams

### **#2. Verify selecting Category in the Most Popular block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Verify the Most Popular block fields|
|4|Сhose sport category|
|5|Verify if conference dropdown is updated|Category dropdown is updated with conferences from a selected Category

### **#3. Verify selecting Conference in the Most Popular block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Verify the Most Popular block fields|
|4|Сhose Conference|
|5|Verify if conference dropdown is updated|Team dropdown is updated with teams related to a selected Conference

</details>

