### Back to [Social Networks on the portal](../../) feature

# Allow users to share portal news with social networks

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user 
    I want to be able to click on the Share with Social Networks button 
    So that I can share the page I am viewing (current page) with the Social Networks

## Acceptance criteria

    Scenario: A site user clicks on the Share with Social Networks button
    Given I am logged in as a site user

    When I view any page on the site 
    Then I see the following social media buttons at the top of the page in the header: 
      - Facebook icon
      - Twitter icon 
      - Google+ icon
      - “Share” text
    When I click the Facebook icon  
    Then I see a popup window is open and I can share the current page on Facebook
    When I click the Twitter button 
    Then I can share the current page on Twitter 
    When I click the Google+ button
    Then I see a popup window is opened and I can “+1” the current page in Google+

## Mockups

1. User sees Share icons and Follow icons on the regular page of the portal
2. User sees sharing in Facebook example

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Share icons and Follow icons on the regular page of the portal:**

![Share icons and Follow icons on the page](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

**2. User sees sharing in Facebook example:**

![Sharing in Facebook example](/products/sport_news_portal/web_application_features/social_networks/images/sharing_in_facebook_example.png)

</details>

## Test Scenarios

1. Verify social media buttons
2. Verify sharing the current page on Facebook
3. Verify sharing the current page on Twitter
4. Verify ability to ‘+1’ the current page in Google+

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify social media buttons**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe social media buttons|The following social media buttons at the top of the page in the header:<br> - Facebook icon<br> - Twitter icon<br> - Google+ icon<br> - “Share” text

### **#2. Verify sharing the current page on Facebook**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe social media buttons|
|4|Click on the Facebook icon|Then a popup window is opened with the ability to share the current page on Facebook

### **#3. Verify sharing the current page on Twitter**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe social media buttons|
|4|Click on the Twitter button|Then a popup window is opened with the ability to share the current page on Twitter

### **#4. Verify ability to ‘+1’ the current page in Google+**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the user account|
|3|Observe social media buttons|
|4|Click on the click the Google+ button|Then a popup window is opened with the ability to ‘+1’ the current page in Google+

</details>
