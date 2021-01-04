### Back to [Surveys on the portal](../../) feature

# Allow users to participate in the surveys on news pages

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see a survey banner on news pages
    So that I can vote

## Acceptance criteria

<pre>
Scenario: A site user sees a survey banner on news pages
Given I am a site user

When I am on any site page
Then I see the banner with the form of the newest in the <b>Reader pool</b> that contains:
  - Survey active period
  - Question
  - Answer options
  - Active <b>Next</b> question button
  - Disabled <b>See the results</b> button

When I am logged in and click <b>Next</b>
Then I see the next survey

When I am logged in and choose an answer
Then I see the <b>See the results</b> button is active

When I am logged in and click <b>See the results</b> button
Then I see the progress bar for each answer option
  And I see the <b>Back to survey</b> button

When I am logged in and click <b>Back to survey</b> button
Then I see the next survey question
  And the voted previous survey is moved to the <b>Closed</b> tab

When I am not logged in and click <b>Next</b> or try to choose an answer
Then I see the pop-up window "Please log in to vote" with the log-in form
</pre>

## Mockups

1. User sees a banner woth Reader pool and voting form
2. Not authoried user clicked to vote and sees a popup to log in

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a banner woth Reader pool and voting form:**

![User sees a banner woth Reader pool and voting form](/products/sport_news_portal/web_application_features/surveys/images/user_survey_banner.png)

**2. Not authoried user clicked to vote and sees a popup to log in:**

![Not authoried user clicked to vote and sees a popup to log in](/products/sport_news_portal/web_application_features/surveys/images/user_login_popup.png)

</details>

## Test cases

1. Verify the content of Reader Poll banner on the site
2. Verify that logged in user can vote on the survey in  Reader Pool banner
3. Verify that logged in user cannot vote twice on the same survey in Reader Pool banner
4. Verify that not logged in user cannot vote or load next survey on the survey in Reader Pool banner and the message about required login appears

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of Reader Poll banner on the site**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There is a published survey|1) Examine the content of the <b>Reader Pool</b> banner|1) - The <b>Reader Pool</b> banner appears on the right side. </br>- There is a survey question, the date range for voting, answer variants without preselection, active <b>Next</b> button, and disabled <b>See the results</b> button|

### **#2. Verify that logged in user can vote on the survey in  Reader Pool banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There is a published survey|1) Select an answer in the <b>Reader Pool</b> banner</br>2) Click <b>See the results</b></br>3) Click <b>Next</b>|1) The answer is calculated. <b>See the results</b> button is active</br>2) Results of all users voting are shown</br>3) The next survey is loaded

### **#3. Verify that logged in user cannot vote twice on the same survey in Reader Pool banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- There is a published survey</br>- User already voted for this survey|1) Examine the <b>Reader Pool</b> banner|1) Results of all users voting are shown. The <b>Next</b> button is present|

### **#4. Verify that not logged in user cannot vote or load next survey on the survey in Reader Pool banner and the message about required login appears**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There is a published survey|1) Select an answer in the <b>Reader Pool</b> banner</br>2) Click <b>Next</b>|1) "Please log in to vote" popup appears with the link to the log-in page</br>2) "Please log in to vote" popup appears with the link to the log-in page|

</details>
