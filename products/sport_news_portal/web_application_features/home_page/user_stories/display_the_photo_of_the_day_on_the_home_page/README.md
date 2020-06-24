### Back to [Home page of the portal](/../../) feature

# Display the Photo of the Day on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to see Photo of the Day block on the page
    So that I could review a photo of the day

## Acceptance criteria

    Scenario: A site user views Photo of the Day content block on the Home Page
    Given I am logged in as a site user

    When I am on the Home page
    Then I see a Photo of the Day block after main articles
      And I see a large photo (set up by the admin) is displayed along with a title and caption

## Mockups

1. User sees Home Page 

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Home Page:**

![Home Page - user side](/products/sport_news_portal/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test Scenarios

1.  Verify that user can see Photo of the Day

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1.  Verify that user can see Photo of the Day**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in to your user account|User is navigated to home page
|3|Examine photo of the day|The system shows Photo of the Day along with a title and caption block after main articles

</details>
