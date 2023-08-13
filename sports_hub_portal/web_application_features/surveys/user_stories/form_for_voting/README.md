### Back to [Surveys on the portal](../../README.md) feature

# Allow users to participate in surveys on the My surveys page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to vote on the My surveys page in my personal cabinet

## Acceptance criteria

<pre>
<b><i>Scenario: A site user votes on the My surveys page</i></b>

Given I am logged in as a site user

When I visit the <b>My surveys</b> page
Then I see a first survey is active and displays in the <b>Reader Poll</b> on the right side

When I select any of the <b>Opened</b> surveys
Then I see a form in the <b>Reader Poll</b> that contains:
  - Survey active period
  - Question
  - Answer options
  - Active <b>Next</b> question button
  - Disabled <b>See the results</b> button

When I click the <b>Next</b> button
Then I see the next survey

When I choose an answer
Then I see the <b>See the results</b> button is active

When I click the <b>See the results</b> button
Then I see the progress bar for each answer option
  And I see the <b>Back to survey</b> button

When I click the <b>Back to survey</b> button
Then I see the next survey question
  And the previously voted survey is moved to the <b>Closed</b> tab
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a voting form in the <b>Reader Poll</b>
2. Users click the <b>See the results</b> button and see results and the <b>Back to survey</b> button
3. Users see survey results on the <b>Closed</b> tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a voting form in the Reader Poll:**

![Users see a voting form in the Reader Poll](/sports_hub_portal/web_application_features/surveys/images/user_voting_form.png)

**2. Users click the See the results button and see results and the Back to survey button:**

![Users click the See the results button and see results and the Back to survey button](/sports_hub_portal/web_application_features/surveys/images/user_back_to_survey.png)

**3. Users see survey results on the Closed tab:**

![Users see survey results on the Closed tab](/sports_hub_portal/web_application_features/surveys/images/user_closed_tab.png)

</details>

## Test cases

1. Verify the content of the <b>Reader Poll</b> block on the <b>My surveys</b> page of the Personal cabinet
2. Verify that users can vote on the survey on the <b>My surveys</b> page of the Personal cabinet
3. Verify that users cannot vote twice on the same survey on the <b>My surveys</b> page of the Personal cabinet

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Reader Poll block on the My surveys page of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab</br>- There is a published survey|1) Select any survey</br>2) Examine the content of the <b>Reader Poll</b> section|1) The appropriate <b>Reader Poll</b> block appears on the right side</br>2) There is a question of the survey, the date range for voting, answer variants without preselection, the active <b>Next</b> button, and the disabled <b>See the results</b> button|

### **#2. Verify that users can vote on the survey on the My surveys page of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab</br>- There is a published survey|1) Select any survey</br>2) Select an answer</br>3) Click <b>See the result</b></br>4) Click <b>Back to survey</b>|2) The answer is calculated. The <b>See the result</b> button is active</br>3) Results of all users voting are shown</br>4) <b>Reader Poll</b> for the survey is shown|

### **#3. Verify that users cannot vote twice on the same survey on the My surveys page of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab</br>- There is a published survey</br>- The user has already voted on this survey|1) Examine the <b>Reader Poll</b> section|1) Results of all users voting are shown. The <b>Next</b> button is present|

</details>
