### Back to [Manage advertisements on the portal](../../) feature

# Allow users to see advertisements

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view an advertisement on the top of the right sidebar of the site

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views advertisement on the top of the right sidebar</i></b>

Given I am a site user

When I view a page of the Sport News and the advertisements are configured to be shown by the admin
Then I see an advertisement on the top right of the right sidebar

When the site-wide advertisement is configured
Then I see it on any page of the site

When the category specific advertisement is configured
Then I see it only on the category relevant pages

When there is more than one advertisement configured (site-wide or category specific)
Then advertisements are rotating each 3 seconds in the banner
</pre>

## Mockups

1. User sees ad on the portal (Nike shoes)

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees ad on the portal (Nike shoes):**

![User sees ad on the portal (Nike shoes)](/products/sport_news_portal/web_application_features/manage_ads/images/display_ads.png)

</details>

## Test cases

1. Verify that the user is able to view site-wide ads on any page
2. Verify that user is able to view category-related ads only on specific pages
3. Verify that ads are rotating

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the user is able to view site-wide ads on any page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are advertisements without selected categories|1) Navigate through different pages of the site|1) Users can see advertisements on all pages|

### **#2. Verify that user is able to view category-related ads only on specific pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are advertisements with some selected categories|1) Navigate to the selected category</br>2) Navigate to another category|1) Users can see advertisements</br>2) Users can’t see advertisements|

### **#3. Verify that ads are rotating**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- There are more than one ad in the category or site-wide|1) Go to a category</br>2) Wait 3 seconds</br>3) Examine the right sidebar</br>4) Wait till all ads from the category are shown|3) Ad is changed on the right sidebar</br>4) The first ad is shown again|
</details>
