### Back to [Home page in the application](../../) feature

# Display Photo of the day for users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to see Photo of the day on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the Photo of the day section on the Home page</i></b>

Given I am an user

When I am on the <b>Home</b> page
Then I see the <b>Photo of the day</b> section after the <b>Main articles</b> and <b>Breakdown</b> section
  And I see a large photo is displayed along with a title, caption, and author

When the <b>Photo of the day</b> section is hidden by admin
Then I don't see the <b>Photo of the day</b> section

When the <b>Photo of the day</b> section is unhidden by admin
Then I see the <b>Photo of the day</b> section
</pre>

## Mockups

1. Full <b>Home</b> page
2. Users see <b>Photo of the day</b> section

<details>
  <summary>Click here to see mockups details</summary>

**1. Full Home page:**

![Full Home page](/products/sports_hub_portal/mobile_application_features/home_page/images/home_page.png)

**2. Users see Photo of the day section**

![Users see Photo of the day section](/products/sports_hub_portal/mobile_application_features/home_page/images/application_photo_of_the_day_section.png)

</details>

## Test cases

1. Verify that users can see the <b>Photo of the day</b> section
2. Verify that the hidden <b>Photo of the day</b> section is not shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users can see the Photo of the day section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configures the <b>Photo of the day</b> section</br>- Go to the <b>Home</b> page > <b>Photo of the day</b> section|1) Examine the <b>Photo of the day</b> section on the <b>Home</b> page|1) The <b>Photo of the day</b> section with the title, caption, and author are visible after the <b>Main articles</b> section|

### **#2. Verify that the hidden Photo of the day section is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configures the <b>Photo of the day</b> section</br></br>- Go to the <b>Home</b> page|1) On the <b>Home</b> page, examine the <b>Photo of the day</b> section|1) The <b>Photo of the day</b> section is not present|
</details>
