### Back to [Manage Articles of the portal](/../../) feature

# Allow admin users to delete existing article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As an admin user
    I want to be able to delete the existing article

## Acceptance criteria

    Scenario: An admin user deletes the existing article on the horizontal ellipsis menu icon
    Given I am logged in as an admin user

    When I click the Delete button on the overflow menu icon in the top-right corner of the article in the list
    Then I see confirmation popup with:
      - The question "Are you sure you want to delete the current Article?"
      - The button Yes
      - The button Cancel
    When I click Cancel button
    Then I see the pop up disappear and nothing changes
    When I click Yes button
    Then I see "The article is successfully deleted" popup in case of success or "Something went wrong, please try again" in case of fail, both cases have Cross icon on the right top corner
    When I click on Cross icon
    Then I see the updated list

## Mockups

1. User sees delete article option
2. User sees delete article confirmation popup
3. User sees delete article failure popup
4. User sees delete article success popup

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees delete article option:**

![Delete article Screen](/products/sport_news_portal/web_application_features/manage_articles/images/delete_article_option.png)

**2. User sees delete article confirmation popup:**

![Delete article confirmation popup](/products/sport_news_portal/web_application_features/manage_articles/images/delete_article_confirmation_popup.png)

**3. User sees delete article failure popup:**

![Delete article failure popup](/products/sport_news_portal/web_application_features/manage_articles/images/article_deletion_failure.png)

**4. User sees delete article success popup:**

![Delete article success popup](/products/sport_news_portal/web_application_features/manage_articles/images/article_deleted_popup.png)

</details>

## Test Scenarios

1. Verify that admin can delete an existing article
2. Verify that admin cannot delete an existing article in case of failure
3. Verify that admin can cancel deleting of an existing article

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify that admin can delete an existing article**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|
|6|Click on Delete|The confirmation popup with the question "Are you sure you want to delete the current Article?" appears
|7|Click on Yes button|"The article is successfully deleted" popup is shown in case of success

### **#2. Verify that admin cannot delete an existing article in case of failure**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|
|6|Click on Delete|The confirmation popup with the question "Are you sure you want to delete the current Article?" appears
|7|Click on Yes button|"Something went wrong, please try again" popup is shown

### **#3. Verify that admin can cancel deleting of an existing article**

|#|Steps|Expected Result
------|-------|----------
|1|Go to sport news site|
|2|Log in your admin account|
|3|Click on any sports category link|Admin is redirected to Create Article page
|4|Hover over any article|Overflow menu appears
|5|Click on overflow menu|
|6|Click on Delete|The confirmation popup with the question "Are you sure you want to delete the current Article?" appears
|7|Click on Cancel button|A pop up will disappear and nothing changes

</details>

