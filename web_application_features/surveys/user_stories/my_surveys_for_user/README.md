### Back to [Surveys on the portal](../../README.md) feature

# Allow users to see a list of all surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see a list of all surveys
    So that I can vote

## Acceptance criteria

<pre>
<b><i>Scenario: A site user visits the My surveys page</i></b>

Given I am logged in as a site user

When I click the drop-down button on the right of the profile picture
Then I see the <b>My surveys</b> menu item

When I click <b>My surveys</b>
Then I am taken to a personal cabinet and the <b>My surveys</b> tab is active
  And I see the system displays only published by admin surveys here
  And I see the system displays two tabs: <b>Opened</b> and <b>Closed</b>

When I am on the <b>Opened</b> tab
Then I see a first survey is active and displayed in the <b>Reader Poll</b> on the right side
  And I see the list is sorted by creation date and contains the following columns:
    - Questions
    - Due date
    - Sort by drop-down with options: Newest (selected by default), Most Popular, About to Expire
    - A search icon

When I am on the <b>Closed</b> tab
Then I see the closed surveys and the following columns:
  - Questions
  - Closed date (is sortable)
  - Filter with options: All surveys, Voted
  - A search icon

When I select any survey on the <b>Closed</b> tab
Then I see survey read-only details in <b>Reader Poll</b> on the right side
  And I see the progress bars for each answer

When I click a search icon
Then I see a search field

When I type some text in the field
Then I see the list of surveys is refreshed with matching results

When I select <b>Voted</b> in the filter
Then I see surveys that I have participated in

When I click the <b>Sort by</b> filter on the <b>Opened</b> tab
Then I see the options:
  - Newest (default)
  - Most Popular
  - About to Expire

When I select <b>Most Popular</b>
Then I see surveys are sorted by the number of voted users

When I select <b>About to Expire</b>
Then I see surveys are sorted by the end day
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see a link to the <b>My surveys</b> page
2. Users see the <b>Opened</b> tab on the <b>My surveys</b> page
3. Users see the <b>Closed</b> tab on the <b>My surveys</b> page
4. Users see <b>Sort by</b> options on the <b>Opened</b> tab
5. Users see filter options on the <b>Closed</b> tab
6. Users see a search input field after clicking the search icon

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a link to the My surveys page:**

![Users see a link to the My surveys page](/web_application_features/surveys/images/user_link_to_surveys_page.png)

**2. Users see the Opened tab on the My surveys page:**

![Users see the Opened tab on the My surveys page](/web_application_features/surveys/images/user_voting_form.png)

**3. Users see the Closed tab on the My surveys page:**

![Users see the Closed tab on the My surveys page](/web_application_features/surveys/images/user_closed_tab.png)

**4. Users see Sort by options on the Opened tab:**

![Users see Sort by options on the Opened tab](/web_application_features/surveys/images/user_sort_by_options.png)

**5. Users see filter options on the Closed tab:**

![Users see filter options on the Closed tab](/web_application_features/surveys/images/user_filter_options.png)

**6. Users see a search input field after clicking the search icon:**

![Users see a search input field after clicking the search icon](/web_application_features/surveys/images/user_search_field.png)

</details>

## Test cases

1. Verify the content of the <b>Opened</b> tab on the <b>My surveys</b> page
2. Verify that users can sort surveys by <b>Newest, Most Popular, About to Expire</b> options on the <b>Opened</b> tab on the <b>My surveys</b> page
3. Verify the content of the <b>Closed</b> tab on the <b>My surveys</b> page
4. Verify that users can filter surveys by <b>Voted, All surveys</b> on the <b>Closed</b> tab on the <b>My surveys</b> page
5. Verify that users can sort surveys by <b>Closed date</b> on the <b>Closed</b> tab on the <b>My surveys</b> page

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Opened tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account|1) Click the drop-down near the profile picture</br>2) Select <b>My surveys</b> item</br>3) Examine the <b>Opened</b> tab|2) Personal cabinet opens on the <b>My surveys</b> page</br>3) The <b>Opened</b> tab is opened by default. The <b>Opened</b> tab consists of two columns: <b>Questions</b> and <b>Due date</b>. The list contains all opened surveys for the moment. Surveys are sorted from the newest to oldest|

### **#2. Verify that users can sort surveys by Newest, Most Popular, About to Expire options on the Opened tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Opened</b> tab|1) Select the <b>Sort by</b> link</br>2) Click <b>Most popular</b></br>3) Select the <b>Sort by</b> link</br>4) Click <b>About to Expire</b></br>5) Select the <b>Sort by</b> link</br>6) Click <b>Newest</b></br>|2) Surveys are sorted according to the amount of users voted from the biggest number</br>4) Surveys are sorted according to the end date from the closest one</br>6) Surveys are sorted according to the date of creation from the newest one|

### **#3. Verify the content of the Closed tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Closed</b> tab|1) Examine the <b>Closed</b> tab|1) The <b>Closed</b> tab consists of two columns: <b>Questions</b> and <b>Closed date</b>. The list contains all closed surveys|

### **#4. Verify that users can filter surveys by Voted, All surveys on the Closed tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Closed</b> tab|1) Click a filter icon</br>2) Click <b>Voted</b></br>3) Click a filter icon</br>4) Click <b>All surveys</b>|2) All surveys I have participated in are shown</br>4) All surveys are shown|

### **#5. Verify that users can sort surveys by Closed date on the Closed tab on the My surveys page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with user account</br>- The user is on the <b>My surveys</b> page > <b>Closed</b> tab|1) Click <b>Closed date</b> sort icon</br>2) Click <b>Closed date</b> sort icon once more|1) Surveys are sorted from the oldest close date at the top</br>2) Surveys are sorted from the newest close date at the top|

</details>
