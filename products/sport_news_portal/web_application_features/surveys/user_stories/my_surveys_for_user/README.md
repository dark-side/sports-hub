### Back to [Surveys on the portal](../../) feature

# Allow users to see a list of all surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see a list of all surveys
    So that I can vote

## Acceptance criteria

<pre>
<b><i>Scenario: A site user visits My surveys page</i></b>

Given I am logged in as a site user

When I click the drop-down button on the right of the profile picture
Then I see the <b>My surveys</b> menu item

When I click <b>My surveys</b>
Then I am taken to a personal cabinet and the <b>My surveys</b> tab is active
  And I see the system displays only published by admin surveys here
  And I see the system displays two tabs: <b>Open</b> and <b>Closed</b>

When I am on the <b>Open</b> tab
Then I see a first survey is active and displayed in the <b>Reader pool</b> on the right side
  And I see the list is sorted by creation date and contains columns:
    - Questions
    - Due date
    - Sort by drop-down with options: Newest (selected by default), Most Popular, About to Expire
    - A search icon

When I am on the <b>Closed</b> tab
Then I see the closed surveys and columns:
  - Questions
  - Closed date (is sortable)
  - Filter with options: All surveys, Voted
  - A search icon

When I click on any survey on the <b>Closed</b> tab
Then I see survey read-only details in <b>Reader pool</b> on the right side
  And I see the progress bars for each answer

When I click on a search icon
Then I see a search field

When I type some text in the field
Then I see the list of surveys is refreshed with matching results

When I select <b>Voted</b> in the filter
Then I see the survey that I participated in

When I click the <b>Sort by</b> filter on the <b>Open</b> tab
Then I see the options:
  - Newest (default)
  - Most Popular
  - About to Expire

When I select <b>Most Popular</b>
Then I see the survey is sorted by the number of voted users

When I select <b>About to Expire</b>
Then I see the survey is sorted by the end day
</pre>

## Mockups

1. User sees a link to My surveys page
2. User sees the Open tab on My surveys page
3. User sees the Closed tab My surveys page
4. User sees Sort by options on the Open tab
5. User sees filter options on the Closed tab
6. User clicked search icon and sees an input field

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a link to My surveys page:**

![User sees a link to My surveys page](/products/sport_news_portal/web_application_features/surveys/images/user_link_to_surveys_page.png)

**2. User sees the Open tab on My surveys page:**

![User sees the Open tab on My surveys page](/products/sport_news_portal/web_application_features/surveys/images/user_voting_form.png)

**3. User sees the Closed tab My surveys page:**

![User sees the Closed tab My surveys page](/products/sport_news_portal/web_application_features/surveys/images/user_closed_tab.png)

**4. User sees Sort by options on the Open tab:**

![User sees Sort by options on the Open tab](/products/sport_news_portal/web_application_features/surveys/images/user_sort_by_options.png)

**5. User sees filter options on the Closed tab:**

![User sees filter options on the Closed tab](/products/sport_news_portal/web_application_features/surveys/images/user_filter_options.png)

**6. User clicked search icon and sees an input field:**

![User clicked search icon and sees an input field](/products/sport_news_portal/web_application_features/surveys/images/user_search_field.png)

</details>

## Test cases

1. Verify the content of the Open tab on the My surveys section
2. Verify that user can sort surveys by Newest, Most Popular, About to Expire on the Open tab on My surveys section
3. Verify the content of the Closed tab on the My surveys tab
4. Verify that user can filter surveys by Voted, All surveys on the Closed tab on My surveys section
5. Verify that user can sort surveys by Closed Date on the Closed tab on My surveys section

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Open tab on the My surveys section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account|1) Click on the drop-down near the profile picture</br>2) Click on <b>My surveys</b> item</br>3) Examine the <b>Open</b> tab|2) Personal cabinet is opened on the <b>My surveys</b> page</br>3) Open tab is opened by default. The open tab consists of two columns: <b>Questions</b> and <b>Due Date</b>. The list contains all open surveys for the moment. Surveys are sorted from the newest to oldest|

### **#2. Verify that user can sort surveys by Newest, Most Popular, About to Expire on the Open tab on My surveys section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Open</b> tab|1) Click <b>Sort by</b> link</br>2) Click <b>Most popular</b></br>3) Click <b>Sort by</b> link</br>4) Click <b>About to Expire</b></br>5) Click <b>Sort by</b> link</br>6) Click <b>Newest</b></br>|2) Surveys are sorted according to the amount of users voted from the biggest number</br>4) Surveys are sorted according to the end date from the closest one</br>6) Surveys are sorted according to the date of creation from the newest one|

### **#3. Verify the content of the Closed tab on the My surveys tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Closed</b> tab|1) Examine the <b>Closed</b> tab|1) Closed tab consists of two columns: Questions and Closed date. The list contains all closed surveys|

### **#4. Verify that user can filter surveys by Voted, All surveys on the Closed tab on My surveys section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Closed</b> tab|1) Click a filter icon</br>2) Click <b>Voted</b></br>3) Click a filter icon</br>4) Click <b>All surveys</b>|2) All surveys I have participated in are shown</br>4) All surveys are shown|

### **#5. Verify that user can sort surveys by Closed Date on the Closed tab on My surveys section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by user account</br>- User is on <b>My surveys</b> section -> <b>Closed</b> tab|1) Click <b>Closed date</b> sort icon</br>2) Click <b>Closed date</b> sort icon once more|1) Surveys are sorted from the oldest close date at the top</br>2) Surveys are sorted from the newest close date at the top|

</details>
