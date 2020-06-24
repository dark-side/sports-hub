### Back to [Manage News Partners on the portal](/../../) feature

# Allow admin users to delete the integration with the partner on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user 
    I want to be able to delete the existing integration with the partner

## Acceptance criteria

    Scenario: An admin user deletes the existing integration with the partner on the News Partners page
    Given I am logged in as an admin user

    When I click the Delete link for the needed partner on the News Partners page  
    Then I see confirmation popup with:
      - The question "Are you sure you want to delete the integration with {partner name}?" 
      - The button Yes
      - The button Cancel 
    When I click Cancel button
    Then I see a pop up disappear and nothing changes
    When I click Yes button
    Then I see "The integration is successfully deleted" popup in case of success or "Something went wrong, please try again" in case of fail, both cases have Cross icon on the right top corner 
    When I click on Cross icon
    Then I see the updated list

## Mockups

1. Admin user sees News Partners list
2. Before delete user sees warning popup
3. Admin user sees “Something went wrong” popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![News Partners list](/products/sport_news_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Before delete user sees warning popup:**

![Before delete warning popup](/products/sport_news_portal/web_application_features/manage_news_partners/images/delete_news_partner_warning_popup.png)

**3. Admin user sees “Something went wrong” popup:**

![Something went wrong popup](/products/sport_news_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test Scenarios

1. Verify confirmation popup on clicking Delete on the News Partners page
2. Verify deleting the existing integration with the partner
3. Verify deleting the existing integration with the partner in case of failure
4. Verify cancel button on confirmation popup

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify confirmation popup on clicking Delete on the News Partners page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Click on Delete link|Confirmation popup appears with:<br> - The question "Are you sure you want to delete the integration with {partner name}?"<br> - The Yes button<br> - The Cancel button

### **#2. Verify deleting the existing integration with the partner**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Click on Delete link|Confirmation popup appears with:<br> - The question "Are you sure you want to delete the integration with {partner name}?"<br> - The Yes button<br> - The Cancel button
|5|Click on Yes button|"The integration is successfully deleted" popup appears

### **#3. Verify deleting the existing integration with the partner in case of failure**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in the admin account|
|3|Click on News Partners on the Left Sidebar|
|4|Click on Delete link|Confirmation popup appears with:<br> - The question "Are you sure you want to delete the integration with {partner name}?"<br> - The Yes button<br> - The Cancel button
|5|Click on Yes button and simultaneously imitate some network disconnection|"Something went wrong, please try again" pop up appears

### **#4. Verify cancel button on confirmation popup**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site
|2|Log in the admin account
|3|Click on News Partners on the Left Sidebar
|4|Click on Delete link|Confirmation popup appears with:<br> - The question "Are you sure you want to delete the integration with {partner name}?"<br> - The Yes button<br> - The Cancel button
|5|Click on Cancel button|A pop up will disappear and nothing changes

</details>
