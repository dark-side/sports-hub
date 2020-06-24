### Back to [Home page of the portal](../../) feature

# Display the Main News on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to see Main News on the page 

## Acceptance criteria

    Scenario: A site user views Main News content block on the Home Page
    Given I am logged in as a site user

    When I am on the Home page
    Then I see a main news block at the top of the page
      And I see the block that contains rotating configured articles
      And I see that each article contains the next information:
        - photo
        - headline
        - caption
        - category for the article’s site section
        - link to the article page 
      And I see the active (large photo) article changes (rotating between the configured articles) every three second
      And I see numbered navigation to manually change the active article
    When I hover over the active article photo
    Then I see the automatic rotation is paused until I move my mouse off of the active article photo 
    When I click on any of the articles
    Then I am taken to that article’s page 

## Mockups

1. User sees Home Page 

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Home Page:**

![Home Page - user side](/products/sport_news_portal/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test Scenarios

1. Verify that featured content block at home page contains 5 rotating articles
2. Verify that each configured article contains all the needed information
3. Verify the active photo article changing period
4. Verify hovering over the active article photo

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that featured content block at home page contains 5 rotating articles**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Observe the home page featured content block|Featured content block on home page contains 5 rotating articles

### **#2. Verify that each configured article contains all the needed information**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Click on any configured articles of featured content block|
|4|Examine what information contain each article|Each article contains the next information:<br> - photo<br> - headline<br> - caption<br> - category for the article’s site section<br> - link to the article page 

### **#3. Verify the active photo article changing period**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Examine the rotating article photo changing on home page|The active (large photo) article changes (rotating between the configured articles) every three second

### **#4. Verify hovering over the active article photo**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|
|3|Examine the rotating article photo changing on home page|The active (large photo) article changes (rotating between the configured articles) every three second
|4|Hover over the active article photo|The automatic rotation is paused until I move my mouse off of the active article photo

</details>
