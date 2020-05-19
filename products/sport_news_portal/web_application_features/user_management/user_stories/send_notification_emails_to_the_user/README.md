### Back to [User Management on the portal](/../../) feature

# Allow admin user to send notification emails to the users on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to be able to receive notification to my email
    So that I know if I was blocked, activated, got/lost admin permissions

## Acceptance criteria

    Scenario: A site user receives notification to my email
    Given I am logged in as a site user
	
    When I am blocked, activated, got/lost admin permissions by the admin user
    Then I see an email with corresponding message

## Mockups

1. User sees user example of the email style and structure

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees user example of the email style and structure:**

![Example of the email](/products/sport_news_portal/web_application_features/user_management/images/mail_style_example.png)

</details>

## Test Scenarios

1. Verify that users receive notification emails if they were blocked
2. Verify that users receive notification emails if they were activated
3. Verify that users receive notification emails if they were given admin permissions
4. Verify that users receive notification emails if they were taken back admin permissions

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that users receive notification emails if they were blocked**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Block some test user|
|6|Check the test user’s emails|User received notification emails of being blocked

### **#2. Verify that users receive notification emails if they were activated**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Activate some test user|
|6|Check the test user’s emails|User received notification emails of being blocked

### **#3. Verify that users receive notification emails if they were given admin permissions**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Give admin permissions some test user|
|6|Check the test user’s emails|User received notification emails of being blocked

### **#4. Verify that users receive notification emails if they were taken back admin permissions**

|#|Steps|Expected Result
------|-------|----------
|1|Go to Sport News site|
|2|Log in your admin account|
|3|Click on User Management menu item|
|4|Go to User Management page|
|5|Take back admin permissions of some test users|
|6|Check the test user’s emails|User received notification emails of being taken back admin permissions

</details>
