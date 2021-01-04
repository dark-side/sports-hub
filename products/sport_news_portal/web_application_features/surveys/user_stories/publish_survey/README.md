### Back to [Surveys on the portal](../../) feature

# Allow admin to publish the surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to publish the surveys
    So that the users can see them and vote

## Acceptance criteria

<pre>
Scenario: An admin user publishes the survey
Given I am logged in as an admin user

When I am on the <b>Surveys</b> page and view the <b>Open</b> tab
Then I see a <b>Publish</b> action for <b>Not published</b> surveys

When I click <b>Publish</b>
Then I see a success message
  And I see the survey status is changed to <b>Published</b>
  And I the survey is visible for the site users

When I click on a <b>Published</b> survey
Then I see a survey read-only details in the <b>Reader pool</b> without any action buttons
  And I see the progress bars for each answer
</pre>

## Mockups

1. Admin user sees actions for not published survey and published survey in the Reader pool

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for not published survey and published survey in the Reader pool:**

![Admin user sees actions for not published survey and published survey in the Reader pool](/products/sport_news_portal/web_application_features/surveys/images/admin_non_published_actions.png)

</details>

## Test cases

1. Verify that admin can publish a not published survey
2. Verify that it is not possible to edit a published survey

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can publish a not published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is not published survey|1) Select not published survey</br>2) Click the <b>Not published</b> state</br>3) Select <b>Publish</b> action</br>|3) The survey changes state to <b>Published</b>. The survey is available for users to vote|

### **#2. Verify that it is not possible to edit a published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey|1) Click published survey|1) In the <b>Reader poll</b> section on the right side, information about the survey appears. There is a name, answers to the survey, and percentage for each answer. No actions appear|

</details>
