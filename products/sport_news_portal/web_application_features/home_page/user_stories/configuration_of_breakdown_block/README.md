### Back to [Home page of the portal](../../) feature

# Allow admin user to configure Breakdown block

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user 
    I want to be able to set up Breakdown block news for a specific category
    So that the site users can see them on the Home page

## Acceptance criteria

    Scenario: An admin user configures Breakdown block news for a specific category
    Given I am logged as an admin user

    When I am on Home configuration page
    Then I see a Breakdown block after Main News block
      And I see the Breakdown block contains the next dropdown fields:
        - Category - contains a list of all sport categories - required field
        - Conference - contains a list of all conferences
        - Team - contains a list of all teams
      And I see an  “Add One More” link, Delete icon, and show/hide toggle are displayed at the bottom of the block
    When I select Category
    Then I see a Conference dropdown is updated with conferences from a selected Category if any
      And I see a Team dropdown is updated with teams related to a selected Category if any
    When I select Conference
    Then I see a Team dropdown is updated with teams related to a selected Conference if any
    When I click on Add One More
    Then I see a system displays the same breakdown news row and Delete icon, and show/hide toggle in front of it
    When I click on Delete icon
    Then I see the second row is being removed from the page
    When I click Save 
    Then I see selected articles are saved to database but not yet published
    When I click Publish
    Then I see All changes are ready to be displayed for the users on the Home Page

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

1. Verify that Breakdown block contains the next dropdown fields
2. Verify selecting Category in Top News
3. Verify selecting Conference in Top News
4. Verify Add one more link at the bottom of the breakdown block
5. Verify deleting breakdown news row
6. Verify saving breakdown news to be displayed on Home page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that Breakdown block contains the next dropdown fields**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Examine dropdown fields in Breakdown block|The Breakdown block contains the next dropdown fields:<br> - Category - contains a list of all sport categories<br> - Conference - contains a list of all conferences<br> - Team - contains a list of all teams

### **#2. Verify selecting Category in Top News**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Verify the Top News block fields|
|4|Сhose sport category|
|5|Verify if category dropdown is updated|Category dropdown is updated with conferences from a selected Category<br>And Team dropdown is updated with teams related to a selected Category

### **#3. Verify selecting Conference in Top News**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Verify the Top News block fields|
|4|Сhose Conference|
|5|Verify if conference dropdown is updated|Conference dropdown is updated with conferences from a selected Category<br>And Team dropdown is updated with teams related to a selected Category

### **#4. Verify Add one more link at the bottom of the breakdown block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Click on Add One More link at the bottom of the breakdown block|Then the system displays the same breakdown news row and Delete Icon in front of it

### **#5. Verify deleting breakdown news row**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Click on Add One More link at the bottom of the breakdown block|Then the system displays the same breakdown news row and Delete Icon in front of it
|4|Click on Delete icon|The system removes the second row from the page

### **#6. Verify saving breakdown news to be displayed on Home page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log into your admin account|
|3|Click on Add One More link at the bottom of the breakdown block|Then the system displays the same breakdown news row and Delete Icon in front of it
|4|Choose the article|
|5|Click on Save|The selected articles are saved to database but not yet published
|6|Click  on Publish|All changes are ready to be displayed for the users on the Home Page

</details>

