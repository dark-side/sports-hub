### Back to [Surveys](../../) feature

# Allow users to participate in surveys on the My surveys page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to vote on the My surveys page in my personal cabinet

## Acceptance criteria

<pre>
<b><i>Scenario: A user submits a survey</i></b>

Given I am logged in as a user on the <b>My surveys</b> page

When I tap the Expand icon for <b>Opened</b> survey
Then I see a voting form
  And I see the form contains a survey active period, question, answer options, the <b>Vote to see results</b> (inactive) and <b>Next</b> buttons

When I choose an answer
Then I see the <b>Vote to see results</b> is active

When I tap <b>Vote to see results</b>
Then I see progress bars of the answers
  And <b>Vote to see results</b> button is inactive

When I tap <b>Next</b>
Then I see the next question to vote
  And the previous survey is moved to the <b>Closed</b> tab if I voted

When I tap <b>Closed</b> tab
Then I see the <b>Closed</b> list contains closed surveys

When I select a survey and tap the Expand icon
Then I see progress bars of the answers
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a voting form in the <b>Opened</b> tab
2. Users selected an answer
3. Users see progress bars of the answers after <b>Vote to see results</b> button click
4. Users see closed survey in the <b>Closed</b> tab

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a voting form in the Opened tab:**

![Users see a voting form in the Opened tab](/sports_hub_portal/mobile_application_features/surveys/images/application_user_voting_form.png)

**2. Users selected an answer:**

![Users selected an answer](/sports_hub_portal/mobile_application_features/surveys/images/application_user_voted.png)

**3. Users see progress bars of the answers after Vote to see results button click:**

![Users see progress bars of the answers after Vote to see results button click](/sports_hub_portal/mobile_application_features/surveys/images/application_user_voting_form_vote_to_see_results.png)

**4. Users see closed survey in the Closed tab:**

![Users see closed survey in the Closed tab](/sports_hub_portal/mobile_application_features/surveys/images/application_user_closed_survey.png)

</details>

## Test cases

1. Verify the content of voting form on the <b>My surveys</b> page
2. Verify that users can vote on the survey on the <b>My surveys</b> page
3. Verify that users cannot vote twice on the same survey in the <b>My surveys</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of voting form on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab</br>- There is a published survey</br>- The user haven’t voted any survey|1) Tap the Expand icon of not voted survey</br>2) Examine the content of voting form|1) The survey is expanded</br>2) There is a name of the survey, date range for voting, answer variants without preselection, the inactive <b>Vote to see results</b> button and active <b>Next</b> button|

### **#2. Verify that users can vote on the survey on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab</br>- There is a published survey</br>- The user hasn’t voted any survey|1) Tap the Expand icon of not voted survey</br>2) Select an answer</br>3) Tap <b>Vote to see results</b>|2)The <b>Vote to see results</b> button is active</br>3) The answer is calculated. Results of all users voting are shown|

### **#3. Verify that users cannot vote twice on the same survey in the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Closed</b> tab</br>- There is a published survey</br>- The user has already voted for this survey|1) Tap the Expand icon of voted survey</br>2) Examine the form|2) Results of all users voting are shown without any buttons|

</details>
