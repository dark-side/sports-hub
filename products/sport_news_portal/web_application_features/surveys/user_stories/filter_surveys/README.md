### Back to [Surveys on the portal](../../) feature

# Allow admin to filter surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to filter opened surveys

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user filters surveys</i></b>

Given I am logged in as an admin user

When I am on the <b>Surveys</b> page and view the <b>Open</b> tab
Then I see the <b>Status</b> filter and a search icon

When I click the <b>Status</b> filter
Then I see the options:
  - All
  - Published
  - Not Published

When I select <b>Published</b>
Then I see only published surveys and their amount

When I select <b>Not published</b>
Then I see only not published surveys and their amount

When I select <b>All</b>
Then I see all surveys and their amount

When I click on a search icon
Then I see a search field

When I type some text in the field
Then I see the list of surveys is refreshed with matching results
</pre>

## Mockups

1. Admin user sees Status filter options
2. Admin user clicked a search icon and sees an input field

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Status filter options:**

![Admin user sees Status filter options](/products/sport_news_portal/web_application_features/surveys/images/admin_status_filter.png)

**2. Admin user clicked a search icon and sees an input field:**

![Admin user clicked a search icon and sees an input field](/products/sport_news_portal/web_application_features/surveys/images/admin_search.png)

</details>

## Test cases

1. Verify that it is possible to filter surveys by the Published state
2. Verify that it is possible to filter surveys by Not Published state
3. Verify that list of surveys is updated according to a search match

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that it is possible to filter surveys by the Published state**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click the <b>Status</b> column label</br>2) Select <b>Published</b>|2) User can see only published surveys in the table|

### **#2. Verify that it is possible to filter surveys by Not Published state**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click the <b>Status</b> column label</br>2) Select <b>Not published</b>|2) User can see only not published surveys are shown in the table|

### **#3. Verify that list of surveys is updated according to a search match**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click on a search icon</br>2) Type some text to the field|1) An input field appears</br>2) The list of surveys is updated with match|

</details>
