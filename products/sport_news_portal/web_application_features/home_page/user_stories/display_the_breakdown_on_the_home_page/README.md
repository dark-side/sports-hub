### Back to [Home page of the portal](/../../) feature

# Display the Breakdown block on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to see Breakdown block on the page
    So that I could read the news

## Acceptance criteria

    Scenario: A site user views Breakdown content block on the Home Page
    Given I am logged in as a site user

    When I am on the Home page
    Then I see a Breakdown block after main articles
      And I see the block contains text Breakdown
      And I see 4 articles for configured categories and in the configured order
      And I see for each article: 
        - Photo
        - Headline
        - Caption - for the 2 secondary articles
    When I click on any of the article photos, headlines, or captions 
    Then I am taken to the article page

## Mockups

1. User sees Home Page 

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Home Page:**

![Home Page - user side](/products/sport_news_portal/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test Scenarios

1. Verify breakdown block text articles’ content
2. Verify clicking on the article photo in breakdown block
3. Verify clicking on the article headline in breakdown block
4. Verify clicking on the article caption in breakdown block

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify breakdown block text articles’ content**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport site news|
|2|Log in to your user account|
|3|Examine breakdown block after main articles|The system shows Breakdown block after main articles
|4|Examine the content of breakdown block|The block contains text Breakdown and 4 articles for configured categories and in the configured order
|5|Examine the content of articles|Each article show:<br> - Photo<br> - Headline<br> - Caption (for the 2 secondary articles)

### **#2. Verify clicking on the article photo in breakdown block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport site news|
|2|Log in to your user account|
|3|Examine the content of articles in breakdown block|Each article show:<br> - Photo<br> - Headline<br> - Caption (for the 2 secondary articles)
|4|Click on any photo in the article|After clicking on any of the article photos, the user is taken to the article page
|5|Click on any headline|
|6|Click on any caption|

### **#3. Verify clicking on the article headline in breakdown block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport site news|
|2|Log in to your user account|
|3|Examine the content of articles in breakdown block|Each article show:<br> - Photo<br> - Headline<br> - Caption (for the 2 secondary articles)
|4|Click on any headline in the article|After clicking on any of the article headlines user is taken to the article page

### **#4. Verify clicking on the article caption in breakdown block**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport site news|
|2|Log in to your user account|
|3|Examine the content of articles in breakdown block|Each article show:<br> - Photo<br> - Headline<br> - Caption (for the 2 secondary articles)
|4|Click on any caption in the article| After clicking on any of the article captions, the user is taken to the article page

</details>
