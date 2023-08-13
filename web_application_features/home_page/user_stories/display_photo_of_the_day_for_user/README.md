### Back to [Home page of the portal](../../README.md) feature

# Display Photo of the day for site users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see the Photo of the day on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the Photo of the day section on the Home page</i></b>

Given I am a site user

When I am on the <b>Home</b> page
Then I see the <b>Photo of the day</b> section after the <b>Main articles</b> section
  And I see a large photo is displayed along with a title, caption, and author

When the <b>Photo of the day</b> section is hidden by admin
Then I do not see the <b>Photo of the day</b> section
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Home</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Home page:**

![Users see the Home page](/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test cases

1. Verify that users can see the <b>Photo of the day</b> section
2. Verify that the hidden <b>Photo of the day</b> section is not shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users can see the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configured the <b>Photo of the day</b> section</br>- Go to the <b>Home</b> page > <b>Photo of the day</b> section|1) Examine the <b>Photo of the day</b> section on the <b>Home</b> page|1) The <b>Photo of the day</b> section with the title, caption, and author are visible after the <b>Main articles</b> section|

### **#2. Verify that the hidden Photo of the day section is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides the <b>Photo of the day</b> section</br>- Go to the <b>Home</b> page|1) On the <b>Home</b> page, examine the <b>Photo of the day</b> section|1) The <b>Photo of the day</b> section is not present|

</details>
