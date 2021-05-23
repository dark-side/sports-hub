### Back to [Advertisements](../../) feature

# Allow users to see advertisements

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view an advertisement on the top of banners after the main content of the page

## Acceptance criteria

<pre>
<b><i>Scenario: A user views advertisement on the top of banners after the main content of the page</i></b>

Given I am a user

When I view a page of the application and the advertisements are configured to be shown by the admin
Then I see an advertisement on the top of banners after the main content of the page

When the application-wide advertisement is configured
Then I see it on any page of the application

When the category specific advertisement is configured
Then I see it only on the category relevant pages

When there is more than one advertisement configured (application-wide or category specific)
Then advertisements are rotating each 3 seconds in the banner
</pre>

## Mockups

1. Users see ad posted in NBA (Nike shoes)

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see ad posted in NBA (Nike shoes):**

![ Users see ad posted in NBA (Nike shoes)](/products/sports_hub_portal/mobile_application_features/advertisements/images/display_ads.png)

</details>

## Test cases

1. Verify that users are able to view application-wide ads on any page
2. Verify that users are able to view category-related ads only on specific pages
3. Verify that ads are rotating

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users are able to view application-wide ads on any page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are advertisements without selected categories|1) Navigate through different pages of the application|1) Users can see advertisements on all pages|

### **#2. Verify that users are able to view category-related ads only on specific pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are advertisements with some selected categories|1) Navigate to the selected category</br>2) Navigate to another category|1) Users can see advertisements</br>2) Users can’t see advertisements|

### **#3. Verify that ads are rotating**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are more than one ad in the category or application-wide|1) Go to the category</br>2) Wait for 3 seconds</br>3) Examine the right sidebar</br>4) Wait till all ads from the category are shown|3) Ad is changed in the section</br>4) The first ad is shown again|
</details>
