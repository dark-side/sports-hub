### Back to [Surveys on the portal](../../) feature

# Allow admin to publish surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to publish surveys
    So that users can see them and vote

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user publishes the survey</i></b>

Given I am logged in as an admin user

When I am on the <b>Surveys</b> page and view the <b>Opened</b> tab
Then I see a <b>Publish</b> action for <b>Not published</b> surveys

When I click <b>Publish</b>
Then I see a success message
  And I see the survey status is changed to <b>Published</b>
  And the survey is visible for site users

When I select a <b>Published</b> survey
Then I see a survey read-only details in the <b>Reader Poll</b> without any action buttons
  And I see the progress bars for each answer
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees actions for unpublished and published surveys in the <b>Reader Poll</b>

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees actions for unpublished and published surveys in the Reader Poll:**

![Admin user sees actions for unpublished and published surveys in the Reader Poll](/sports_hub_portal/web_application_features/surveys/images/admin_non_published_actions.png)

</details>

## Test cases

1. Verify that admin can publish the unpublished survey
2. Verify that it is not possible to edit the published survey

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin can publish the unpublished survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is an unpublished survey|1) Select the unpublished survey</br>2) Click the <b>Not published</b> status</br>3) Select <b>Publish</b> action</br>|3) The survey status changes to <b>Published</b>. The survey is available for users to vote|

### **#2. Verify that it is not possible to edit the published survey**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page</br>- There is a published survey|1) Select the published survey|1) In the <b>Reader Poll</b> section on the right side, information about the survey appears. There is a name, answers to the survey, and percentage for each answer. No actions appear|

</details>
