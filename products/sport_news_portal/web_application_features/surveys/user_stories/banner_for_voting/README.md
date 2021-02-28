### Back to [Surveys on the portal](../../) feature

# Allow users to participate in surveys on news pages

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
<b><i>Scenario: A site user sees a survey banner on news pages</i></b>

Given I am a site user

When I am on any site page
Then I see the banner with the form of the newest <b>Reader Poll</b> that contains:
  - Survey active period
  - Question
  - Answer options
  - Active <b>Next</b> question button
  - Disabled <b>See the results</b> button

When I am logged in and click <b>Next</b>
Then I see the next survey

When I am logged in and choose an answer
Then I see the <b>See the results</b> button is active

When I am logged in and click the <b>See the results</b> button
Then I see the progress bar for each answer option
  And I see the <b>Back to survey</b> button

When I am logged in and click the <b>Back to survey</b> button
Then I see the next survey question
  And the previously voted survey is moved to the <b>Closed</b> tab

When I am not logged in and click <b>Next</b> or try to choose an answer
Then I see the pop-up window "Please log in to vote" with the log-in form
</pre>

## Mockups

1. Users see a banner with <b>Reader Poll</b> and voting form
2. Unauthoried users click to vote and see a pop-up window to log in

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a banner with Reader Poll and voting form:**

![Users see a banner with Reader Poll and voting form](/products/sport_news_portal/web_application_features/surveys/images/user_survey_banner.png)

**2. Unauthoried users click to vote and see a pop-up window to log in:**

![Unauthoried users click to vote and see a pop-up window to log in](/products/sport_news_portal/web_application_features/surveys/images/user_login_popup.png)

</details>

## Test cases

1. Verify the content of the <b>Reader Poll</b> banner on the site
2. Verify that logged-in users can vote on the survey in the <b>Reader Poll</b> banner
3. Verify that logged-in users cannot vote twice on the same survey in the <b>Reader Poll</b> banner
4. Verify that not logged-in users cannot vote on the survey or load the next one in the <b>Reader Poll</b> banner and a pop-up window to log in appears

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Reader Poll banner on the site**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There is a published survey|1) Examine the content of the <b>Reader Poll</b> banner|1) - The <b>Reader Poll</b> banner appears on the right side</br>- There is a survey question, the date range for voting, answer variants without preselection, the active <b>Next</b> button, and the disabled <b>See the results</b> button|

### **#2. Verify that logged-in users can vote on the survey in the Reader Poll banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is a published survey|1) Select an answer in the <b>Reader Poll</b> banner</br>2) Click <b>See the results</b></br>3) Click <b>Next</b>|1) The answer is calculated. The <b>See the results</b> button is active</br>2) Results of all users voting are shown</br>3) The next survey is loaded

### **#3. Verify that logged-in users cannot vote twice on the same survey in the Reader Poll banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- There is a published survey</br>- The user has already voted on this survey|1) Examine the <b>Reader Poll</b> banner|1) Results of all users voting are shown. The <b>Next</b> button is present|

### **#4. Verify that not logged-in users cannot vote on the survey or load the next one in the Reader Poll banner and a pop-up window to log in appears**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There is a published survey|1) Select an answer in the <b>Reader Poll</b> banner</br>2) Click <b>Next</b>|1)  "Please log in to your account to vote" pop-up window  appears with the link to the log-in page</br>2) "Please log in to your account to vote" pop-up window appears with the link to the log-in page|

</details>
