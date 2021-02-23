### Back to [The most popular/commented articles on the portal](../../) feature

# Allow admin user to configure the Most commented section

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure the Most commented section

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures the Most commented section for the whole site from the Home page</i></b>

Given I am logged in as an admin user

When I am on the <b>Home</b> configuration page
Then I see the <b>Most commented</b> section after the <b>Photo of the day</b> section
  And I see the <b>Most commented</b> section contains the following:
    - From the period - drop-down list with <b>Day, Weak, Month, and Year</b> values (<b>Month</b> is the default value)
And I see the <b>Show on the main page</b> toggle is displayed

When I change the period
Then news only from that period is selected to be shown for the user

When I click the <b>Show on the main page</b> toggle
Then the toggle changes to <b>Hide on the main page</b>
  And the whole <b>Most commented</b> section is not shown for users
  And <b>From the period</b> is not visible in this section

When I click the <b>Hide on the main page</b> toggle
Then the toggle changes to <b>Show on the main page</b>
  And the whole <b>Most commented</b> section is shown for users
  And <b>From the period</b> is visible in this section

<i>Note: The most commented articles have the largest number of comments during a selected period of time in the whole news scope for the active page. This section is configured for the whole site and is context-sensitive.</i>
</pre>

## Mockups

1. Admin sees the <b>Most commented</b> section configuration
2. Admin user sees period configuration drop-down list

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin sees the Most commented section configuration:**

![Admin sees the Most commented section configuration](/products/sport_news_portal/web_application_features/most_popular_and_commented/images/most_popular_commented_configuration.png)

**2. Admin user sees period configuration drop-down list:**

![Admin user sees period configuration drop-down list](/products/sport_news_portal/web_application_features/most_popular_and_commented/images/most_popular_commented_configuration_period.png)

</details>

## Test cases

1. Verify that <b>From the period</b> drop-down list can be configured for the <b>Most commented</b> section
2. Verify that the <b>Most commented</b> section can be hidden from users view
3. Verify that the <b>Most commented</b> section can be visible to users view

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that From the period drop-down list can be configured for the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Most commented</b> section|1) Click <b>From the period</b> drop-down list</br>2) Select <b>Day, Week, Month</b>, or <b>Year</b> value|2) The <b>Most commented</b> section displays the most visited last day, week, month, or year articles|

### **#2. Verify that the Most commented section can be hidden from users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Most commented</b> section</br>- There is the <b>Show on the main page</b> toggle|1) Examine the <b>Most commented</b> section</br>2) Click the <b>Show on the main page</b> toggle|2) The toggle changes to <b>Hide on the main page</b>. The <b>Most commented</b> section is not visible to users on all pages|

### **#3. Verify that the Most commented section can be visible to users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Log in with admin account</br>- Go to the <b>Home</b> configuration page > <b>Most commented</b> section</br>- There is the <b>Hide on the main page</b> toggle|1) Examine the <b>Most commented</b> section</br>2) Click the <b>Hide on the main page</b> toggle|2) The Most commented section is visible to users|
</details>
