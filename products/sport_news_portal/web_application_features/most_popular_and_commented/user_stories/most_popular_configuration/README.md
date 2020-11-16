### Back to [Most Popular/Commented articles on the portal](../../) feature

# Allow admin user to configure the Most popular section

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure the Most popular section

## Acceptance criteria

<pre>
Scenario: An admin user configures the Most popular section for the whole site from the home page (most popular articles are the most visited ones during a selected period of time in the whole news scope for the active page)
Given I am logged in as an admin user

<i>Note: This section is configured for the whole site and is context-sensitive.</i>

When I am on the <b>Home</b> configuration page
Then I see the <b>Most popular</b> section after the <b>Photo of the day</b> section
  And I see the <b>Most popular</b> section contains the following:
    - From the period - drop-down list with <b>Day, Weak, Month, and Year</b> values (Month is the default value)
And I see the <b>Show on the main page</b> toggle is displayed

When I change the period
Then news only from that period are selected to be shown for the user

When I click <b>Show on the main page</b> toggle
Then the toggle changes to the <b>Hide on the main page</b>
  And the whole <b>Most popular</b> section is not shown for the users
  And <b>From the period</b> is not visible for this section

When I click <b>Hide on the main page</b> toggle
Then the toggle changes to the <b>Show on the main page</b>
  And the whole Most popular section is shown for the users
  And <b>From the period</b> is visible for this section
</pre>

## Mockups

1. Admin sees most popular section configuration
2. Admin user sees period configuration dropdown

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin sees most popular section configuration:**

![Admin sees most popular section configuration](/products/sport_news_portal/web_application_features/most_popular_and_commented/images/most_popular_commented_configuration.png)

**2. Admin user sees period configuration dropdown:**

![Admin user sees period configuration dropdown](/products/sport_news_portal/web_application_features/most_popular_and_commented/images/most_popular_commentable_configuration_period.png)

</details>

## Test cases

1. Verify that the From the period can be configured for the Most popular section
2. Verify that the Most popular section can be hidden for users view
3. Verify that the Most popular section can be unhidden for users view

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the From the period can be configured for the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News Home page</br>- Log in by admin account</br>- Go to the Home configuration page -> Most popular section|1) Click From the period drop-down</br>2) Select Day/Week/Month/Year value|2) The Most popular section displays the most visited last day/week/month/year articles|

### **#2. Verify that the Most popular section can be hidden for users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News Home page</br>- Log in by admin account</br>- Go to the Home configuration page -> Most popular section</br>- There is <b>Show on the main page</b> toggle|1) Examine the Most popular section</br>2) Click <b>Show on the main page</b> toggle|2) Toggle changes to the Hide on the main page. The Most popular section is not visible for users on all pages|

### **#3. Verify that the Most popular section can be unhidden for users view**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News Home page</br>- Log in by admin account</br>- Go to the Home configuration page -> Most popular section</br>- There is <b>Hide on the main page</b> toggle|1) Examine the Most popular section</br>2) Click <b>Hide on the main page</b> toggle|2) The Most popular section is visible for users|
</details>
