### Back to [Site Footer of the portal](/../../) feature

# Allow users to Newsletter subscription

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to subscribe to a Sport News site
    So that I can receive an email with the latest sport new

## Acceptance criteria

    Scenario: A site user subscribes to a Sport News site
    Given I am logged in as a site user

    When I view a page and the Newsletter subscription block in the Site Footer
    Then I see the following:
      - Heading "Newsletter"
      - "Sign up to receive the latest in sport news" title
      - Input for email address
      - Subscribe button
      - Facebook or Google+ subscription links
    When I fill in a email address and click the Subscribe button
    Then I see the Subscribe button is replaced with a Checkmark confirming my subscription
    The I see the subscription is dependent upon the section of the site you are in, for example:
      - Home page - subscription to all general sports news
      - NBA sport category page - subscription to NBA news
      - Los Angeles Lakers team page - subscription to Los Angeles Lakers team news
    When I click on the Facebook or Google+ subscription link
    Then I see a popup window where I can use my Facebook/Google+ Account to subscribe to Sport News

## Mockups

1. User sees Site Footer
2. User sees subscription successful icon
3. User sees subscription error icon

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Site Footer:**

![Site Footer Screen](/products/sport_news_portal/web_application_features/site_footer/images/site_footer_contact_us.png)

**2. User sees subscription successful icon:**

![Subscription successful icon](/products/sport_news_portal/web_application_features/site_footer/images/subscribed_successfuly.png)

**3. User sees subscription error icon:**

![Subscription error icon](/products/sport_news_portal/web_application_features/site_footer/images/subscription_error.png)

</details>

## Test Scenarios

1. Verify the NEWSLETTER tab displays configuration table with a single row
2. Verify that the Subscribe button functionality for Home page
3. Verify that the Subscribe button functionality for NBA league page
4. Verify that the Subscribe button functionality for Los Angeles Lakers team page
5. Verify clicking on the Facebook or Google+ subscription link

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the NEWSLETTER tab displays configuration table with a single row**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|
|3|Examine NEWSLETTER tab table|The system displays configuration table with a single row:<br>- "Sign up to receive the  latest in sport news"
|4|Verify the input for the email address|"Sign up to receive the latest in sport news" form contains the input for the email address
|5|Verify Subscribe button|Subscribe button is present
|6|Verify the Facebook or Google+ sign up link|The Facebook or Google+ sign up link is present

### **#2. Verify that the Subscribe button functionality for Home page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|User is navigating to Home page
|3|Examine "Sign up to receive the latest in sport news" in NEWSLETTER tab table|The system displays configuration table with a single row:<br>- "Sign up to receive the latest in sport news"
|4|Type your email address in the input for the email address|
|5|Click on Subscribe button|Subscribe button is replaced with a Checkmark confirming subscription
|6|Verify that you are subscribed to all general sports news|You are subscribed to all general sports news

### **#3. Verify that the Subscribe button functionality for NBA league page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|User is navigating to Home page
|3|Navigate to NBA league page|
|4|Examine "Sign up to receive the latest in sport news" in NEWSLETTER tab table|The system displays configuration table with a single row:<br>- "Sign up to receive the latest in sport news"
|5|Type your email address in the input for the email address|
|6|Click on Subscribe button|Subscribe button is replaced with a Checkmark confirming subscription
|7|Verify that you are subscribed to NBA league news|You are subscribed to NBA league news

### **#4. Verify that the Subscribe button functionality for Los Angeles Lakers team page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|User is navigating to Home page
|3|Navigate to Los Angeles Lakers team page|
|4|Examine "Sign up to receive the latest in sport news" in NEWSLETTER tab table|The system displays configuration table with a single row:<br>- "Sign up to receive the latest in sport news"
|5|Type your email address in the input for the email address|
|6|Click on Subscribe button|Subscribe button is replaced with a Checkmark confirming subscription
|7|Verify that you are subscribed to Los Angeles Lakers team news|You are subscribed to Los Angeles Lakers team news

### **#5. Verify clicking on the Facebook or Google+ subscription link**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your user account|User is navigating to Home page
|3|Examine NEWSLETTER tab table|
|4|Click on the Facebook or Google+ sign up link|A popup window appears where Facebook/Google+ account can be used to subscribe to Sport News

</details>
