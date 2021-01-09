### Back to [Surveys on the portal](../../) feature

# Allow users to participate in the surveys on My surveys page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to vote on My surveys page in my personal cabinet

## Acceptance criteria

<pre>
<b><i>Scenario: A site user votes on My surveys page</i></b>

Given I am logged in as a site user

When I visit <b>My surveys</b> page
Then I see a first survey is active and displayed in the <b>Reader pool</b> on the right side

When I click on any of the <b>Open</b> surveys
Then I see a form in the <b>Reader pool</b> that contains:
  - Survey active period
  - Question
  - Answer options
  - Active <b>Next</b> question button
  - Disabled <b>See the results</b> button

When I click <b>Next</b> button
Then I see the next survey

When I choose an answer
Then I see the <b>See the results</b> button is active

When I click <b>See the results</b> button
Then I see the progress bar for each answer option
  And I see the <b>Back to survey</b> button

When I click <b>Back to survey</b> button
Then I see the next survey question
  And the voted previous survey is moved to the <b>Closed</b> tab
</pre>

## Mockups

1. User sees a voting form in the Reader pool
2. User clicked See the results button and sees results and Back to survey button
3. User sees survey results on the Closed tab

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a voting form in the Reader pool:**

![User sees a voting form in the Reader pool](/products/sport_news_portal/web_application_features/surveys/images/user_voting_form.png)

**2. User clicked See the results button and sees results and Back to survey button:**

![User clicked See the results button and sees results and Back to survey button](/products/sport_news_portal/web_application_features/surveys/images/user_back_to_survey.png)

**3. User sees survey results on the Closed tab:**

![User sees survey results on the Closed tab](/products/sport_news_portal/web_application_features/surveys/images/user_closed_tab.png)

</details>

## Test cases

1. Verify the content of Reader Poll block on My surveys section of the Personal cabinet
2. Verify the content of Reader Poll block on My surveys section of the Personal cabinet
3. Verify that user can vote on the survey in My surveys section of the Personal cabinet
4. Verify that user cannot vote twice on the same survey in My surveys section of the Personal cabinet

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of Reader Poll block on My surveys section of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Open</b> tab</br>- There is a published survey|1) Click on any survey</br>2) Examine the content of the <b>Reader pool</b> section|1) The appropriate <b>Reader pool</b> block appears on the right side</br>2) There is a name of the survey, the date range for voting, answer variants without preselection, active <b>Next</b> button, and disabled <b>See the results</b> button|

### **#2. Verify the content of Reader Poll block on My surveys section of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Open</b> tab</br>- There is a published survey|1) Click on any survey</br>2) Examine the content of the <b>Reader pool</b> section|1) The appropriate <b>Reader pool</b> block appears on the right side</br>2) There is a question of the survey, the date range for voting, answer variants without preselection, active <b>Next</b> button, and disabled <b>See the results</b> button|

### **#3. Verify that user can vote on the survey in My surveys section of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Open</b> tab</br>- There is a published survey|1) Click on any survey</br>2) Select an answer</br>3) Click <b>See the result</b></br>4) Click <b>Back to survey</b>|2) The answer is calculated. <b>See the result</b> button is active</br>3) Results of all users voting is shown</br>4) <b>Reader pool</b> for the survey is shown|

### **#4. Verify that user cannot vote twice on the same survey in My surveys section of the Personal cabinet**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Open</b> tab</br>- There is a published survey</br>- User already voted for this survey|1) Examine the <b>Reader pool</b> section|1) Results of all users voting are shown. The <b>Next</b> button is present|

</details>
