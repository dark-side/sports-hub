### Back to [Newsletter Email](../../) feature

# Allow users to receive newsletter email

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to receive a newsletter email
    So that I can read the latest sport news

## Acceptance criteria

    Scenario: A site user receives a newsletter email
    Given I am a site user

    When I am subscribed to receive newsletter email about sport news
    Then I see a daily email from Sport News site
    When I am subscribed to receive all sport news
    Then I see the email that I receive looks like Mockup #1 (General news email)
      And I see email contains most recently added articles to the Sport News site
    When I am subscribed to receive sport news articles related to sport category or team
    Then I see the email that I receive contains news only about the sport category/subcategory/team that I’m subscribed to
      And I see the email content looks like Mockup #2 (sport category/subcategory/team email)
      And I see email contains most recently added articles added to the subscribed sport category/subcategory/team
    When I click on Go To Read button in the general news email
    Then I am taken to a home page of the Sport News site
    When I click on Go To Read button in the sport category/team news email
    Then I am taken to a sport category or team page of the Sport News site

## Mockups

1. User newsletter email

<details>
  <summary>Click here to see mockups details</summary>

**1. User newsletter email:**

![Newsletter email Screen](/products/sport_news_portal/web_application_features/newsletter_email/images/news_email.png)

</details>

## Test Scenarios

1. Verify that the Subscribe button functionality for Home page
2. Verify "Go To Read" button in the sport category/team news email
3. Verify "Go To Read" button in the general news email

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that the Subscribe button functionality for Home page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|User is navigating to Home page
|3|Examine "Sign up to receive the latest in sport news" in NEWSLETTER tab table|The system displays configuration table with a single row: "Sign up to receive the  latest in sport news"
|4|Type your email address in the input for the email address|
|5|Click on Subscribe button|Subscribe button is replaced with a Checkmark confirming subscription
|6|Verify that you are subscribed to all general sports news|You are subscribed to all general sports news
|7|Go to your email and examine if you get newsletter email|Daily email from Sport News site is inbox

### **#2. Verify "Go To Read" button in the sport category/team news email**

|#|Steps|Expected Result
------|-------|----------
|1|Go to your user’s email (note: user should be subscribed to receiving news letter email about sport news (sport category/team news))|
|2|Open Daily email from Sport site that is inbox|
|3|Click on "Go To Read" button|User is taken to a sport category or team page of the Sport News site

### **#3. Verify "Go To Read" button in the general news email**

|#|Steps|Expected Result
------|-------|----------
|1|Go to your user’s email (note: user should be subscribed to receiving news letter email about all sport news)|
|2|Open Daily email from Sport site that is inbox|
|3|Click on "Go To Read" button|User is taken to a home page of the Sport News site

</details>
