### Back to [Manage teams on the portal](/../../) feature

# Allow admin users to delete the existing Team/Player

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to delete the existing Team/Player

## Acceptance criteria

    Scenario: An admin user deletes the existing Team/Player in the right side of  the record
    Given I am logged in as an admin user

    When I click the Trash icon on the right side of  the record
    Then I see confirmation popup with:
      - The question "Are you sure you want to delete the current Team/Player?"
      - The button Yes
      - The Cancel button
    When I click Cancel button
    Then I see a pop up will disappear and nothing changes
    When I click Yes button
    Then I see "Your team is successfully deleted" popup in case of success or "Something went wrong, please try again" in case of fail, both cases have Cross icon on the right top corner
    When I click on Cross icon
    Then I see the updated list

## Mockups

1. User sees delete team confirmation popup
2. User sees teams deleted popup
3. User sees something went wrong popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees delete team confirmation popup:**

![Delete team confirmation popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/delete_team_confirmation_popup.png)

**2. User sees teams deleted popup:**

![Team deleted popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/team_is_deleted_popup.png)

**3. User sees something went wrong popup:**

![Something went wrong popup](/products/sport_news_portal/web_application_features/manage_the_teams/images/something_went_wrong_popup.png)

</details>

## Test Scenarios

1. Verify deleting of the existing Team/Player
2. Verify clicking on cancel button while the process of deleting the existing Team/Player
3. Verify "Something went wrong, please try again" popup in case of fail during the delete confirmation fail

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify deleting of the existing Team/Player**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Trash icon on the right side of the record|Confirmation popup with the question "Are you sure you want to delete the current Team/Player?" , the button Yes and The Cancel button are shown
|5|Click on the Yes button|"Your team is successfully deleted" popup in case of success is shown
|6|Click on Cross icon|The existing Team/Player is deleted

### **#2. Verify clicking on cancel button while the process of deleting the existing Team/Player**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Trash icon on the right side of the record|Confirmation popup with the question "Are you sure you want to delete the current Team/Player?" , the button Yes and The Cancel button are shown
|5|Click on the Cancel button|A pop up will disappear and nothing have been changed

### **#3. Verify "Something went wrong, please try again" popup in case of fail during the delete confirmation fail**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on Teams icon on the left sidebar|Admin user is navigated to teams page
|4|Click on the Trash icon on the right side of the record|Confirmation popup with the question "Are you sure you want to delete the current Team/Player?" , the button Yes and The Cancel button are shown
|5|On clicking on OK button try to imitate some network connection loses for few seconds and stabilize it again|A pop up will disappear and nothing have been changed

</details>
