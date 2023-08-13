### Back to [Surveys on the portal](../../README.md) feature

# Allow admin to filter surveys

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to filter opened surveys

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user filters surveys</i></b>

Given I am logged in as an admin user

When I am on the <b>Surveys</b> page and view the <b>Opened</b> tab
Then I see the <b>Status</b> filter and a search icon

When I click the <b>Status</b> filter
Then I see the options:
  - All
  - Published
  - Not Published

When I select <b>Published</b>
Then I see only published surveys and their amount

When I select <b>Not published</b>
Then I see only unpublished surveys and their amount

When I select <b>All</b>
Then I see all surveys and their amount

When I click a search icon
Then I see a search field

When I type some text in the field
Then I see the list of surveys is refreshed with matching results
(<i>Search can start when the first symbol is entered or when at least 3 symbols are entered</i>)
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>Status</b> filter options
2. Admin user sees a search input field after clicking the search icon

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Status filter options:**

![Admin user sees Status filter options](/sports_hub_portal/web_application_features/surveys/images/admin_status_filter.png)

**2. Admin user sees a search input field after clicking the search icon:**

![Admin user sees a search input field after clicking the search icon](/sports_hub_portal/web_application_features/surveys/images/admin_search.png)

</details>

## Test cases

1. Verify that it is possible to filter surveys by the <b>Published</b> status
2. Verify that it is possible to filter surveys by the <b>Not published</b> status
3. Verify that list of surveys is updated according to a search match

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that it is possible to filter surveys by the Published status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click the <b>Status</b> column label</br>2) Select <b>Published</b>|2) Users can see only published surveys in the table|

### **#2. Verify that it is possible to filter surveys by the Not published status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click the <b>Status</b> column label</br>2) Select <b>Not published</b>|2) Users can see only unpublished surveys in the table|

### **#3. Verify that list of surveys is updated according to a search match**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Surveys</b> configuration page|1) Click a search icon</br>2) Type some text to the field|1) An input field appears</br>2) The list of surveys is updated with match|

</details>
