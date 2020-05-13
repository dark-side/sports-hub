### Back to [Home page of the portal](/../../) feature

# Allow admin user to configure Main News block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to set up up to 5 main news articles
    So that the site users can see them on the Home page

## Acceptance criteria

    Scenario: An admin user configures main news block on the Home page
    Given I am logged in as an admin user

    When I am on Home configuration page
    Then I see a Main News block at the top of the page
      And I do not see Delete and show/hide toggle in front of single row
    When I click on Add One More four times
    Then I see an Add One More link
    When I select Category
    Then I see a Conference dropdown is updated with conferences from a selected Category if any
      And I see the Team dropdown is updated with teams related to a selected Category if any
    When I select Conference
    Then I see a Team dropdown is updated with teams related to a selected Conference if any 
    When I select 5 main articles and click on Save button
    Then I see that selected articles are saved to database but not yet published
    When I click Publish button
    Then I see a all changes are ready to be displayed for the users on the Home Page

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

1. Verify dropdown fields on Main News block
2. Verify “Add One More” link in Main News block
3. Verify that Delete Icon removes the second row from the page
4. Verify click on “Show on the main page” toggle

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify dropdown fields on Main News block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your admin account|User is navigating to Home page
|3|Observe dropdown fields in Main News block|The Main News block contains next dropdown fields:<br> - Category - contains a list of all sport categories<br> - Conference - contains a list of all conferences<br> - Team - contains a list of all teams<br> - Article - contains a list of all articles

### **#2. Verify “Add One More” link in Main News block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your admin account|
|3|Examine dropdown fields in Main News block|
|4|Click on “Add One More”|Then the system displays one more row with the same dropdown fields and Delete icon in front of the second row

### **#3. Verify that Delete Icon removes the second row from the page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your admin account|
|3|Observe dropdown fields in Main News block|
|4|Click on “Add One More”|Then the system displays one more row with the same dropdown fields and Delete icon in front of the second row
|5|Click on Delete icon|The system removes the second row from the page

### **#4. Verify click on “Show on the main page” toggle**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your admin account|
|3|Click on “Show on the main page” toggle is displayed at the bottom of Main News block|The toggle is changed to “Hide on the main page” toggle and the breaking news articles from main news block are not shown

</details>

