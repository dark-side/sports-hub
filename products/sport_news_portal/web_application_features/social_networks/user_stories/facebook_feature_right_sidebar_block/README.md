### Back to [Social Networks on the portal](../../) feature

# Allow users to view and like the Facebook Feature story on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to view and like the Facebook Feature story at the right sidebar of the site

## Acceptance criteria

    Scenario: A site user views and like the Facebook Feature story at the right sidebar of the site
    Given I am logged in as a site user

    When I view a page with the Facebook Feature block in the right sidebar 
    Then I see a block with the following information pulled from the featured story on the ATS Facebook page: 
      - Heading “Facebook Feature” 
      - Feature story photo 
      - Feature story headline 
      - Link to Like us on Facebook 
      - Facebook “Like” button 
      - Current number of Facebook likes 
    When I click the photo or the Like us on Facebook link 
    Then I am taken to the featured story on the ATS Facebook page 
    When I click the Like us button
    Then I see the Facebook popup where I can comment and like the story

## Mockups

1. User sees Facebook Feature story at the right sidebar of the portal

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Facebook Feature story at the right sidebar of the portal:**

![Facebook Feature story at the right sidebar](/products/sport_news_portal/web_application_features/social_networks/images/share_and_follow_on_page.png)

</details>

## Test Scenarios

1. Verify the content of Facebook block at the left sidebar
2. Verify clicking on the photo or the Like us on Facebook link
3. Verify clicking on the Like button

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify the content of Facebook block at the left sidebar**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Observe the left side block|There is a block with the following information pulled from the ATS Facebook page:<br> - Heading “Facebook Feature”<br> - Feature story photo<br> - Feature story headline<br> - Link to Like us on Facebook<br> - Facebook “Like” button<br> - Current number of Facebook likes

### **#2. Verify clicking on the photo or the Like us on Facebook link**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Observe the left side block|
|4|Click on the the Like on Facebook link|User is taken to the featured story on the ATS Facebook page

### **#3. Verify clicking on the Like button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Observe the left side block|
|4|Click on the the Like button|The Facebook popup appears where I can comment and like the story

</details>
