### Back to [Log In and Sign Up to the portal](/../../) feature

# Allow users to update their personal information

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to update my personal information

## Acceptance criteria

    Scenario: As a site user updates personal information
    Given I'm a site user on Personal page form

    When I type new information to First and Last name, email fields and click on Update Profile
    Then the system saves the changes and immediately update the name at the top of the page
      And I see a message about success
    When I click on Update Profile with empty fields, invalid email or photo with invalid format (only .jpg, .png, .jpeg, .tif are allowed)
    Then I see validation messages

## Mockups

1. User sees a profile page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a profile page:**

![Profile Screen](/products/sport_news_portal/web_application_features/log_in_and_sign_up/images/user_profile_page.png)

</details>

## Test Scenarios

1. Verify ability to update personal information

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify ability to update personal information**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your user account|
|3|Click on a drop-down menu next to user's avatar at the top of the page|
|4|Click on View Profile link button|
|5|Change information in Last Name, First Name and Email field and upload a new photo with a valid format|
|6|Click on the Update Profile button|The system saves the changes and immediately update the name at the top of the page

</details>
