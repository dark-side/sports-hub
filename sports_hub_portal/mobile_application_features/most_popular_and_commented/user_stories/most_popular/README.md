### Back to [The most popular/commented articles](../../) feature

# Allow user to view the most popular articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view the Most popular section 
    So that I can read articles that have the highest number of views during the period configured by admin (day, week, month, year)

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the Most popular section</i></b>

Given I am a user

When I view a page with the <b>Most popular</b> section
Then I see this section has a list with 3 most popular articles (most popular based on page views in the configured period)
  And I see that each article has:
    - Thumbnail photo
    - Headline (on the right from the photo)
    - Caption (under Headline)

When I select an article
Then I am taken to the article page
  And the <b>Most popular</b> section is context-sensitive which means:
    - Home page contains the most popular articles from the whole articles list
    - Any other page contains the most popular articles that belong to a category, conference, or team of the current page

When the <b>Most popular</b> section is hidden by admin
Then I don’t see the <b>Most popular</b> section on any page where it can be present

When the <b>Most popular</b> section is unhidden by admin
Then I see the <b>Most popular</b> section on any page where it can be present
</pre>

## Mockups

1. Users see the <b>Most popular</b> articles section
2. Full Home page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Most popular articles section:**

![Users see the Most popular articles section](/products/sports_hub_portal/mobile_application_features/most_popular_and_commented/images/application_most_popular_section.png)

**2. Full Home page:**

![Full Home page](/products/sports_hub_portal/mobile_application_features/most_popular_and_commented/images/home_page.png)

</details>

## Test cases

1. Verify that user can see the <b>Most popular</b> section
2. Verify that user can see articles only for the configured period in the <b>Most popular</b> section
3. Verify that user can’t see the hidden <b>Most popular</b> section
4. Verify that the user is redirected to the proper article by selecting the article in the <b>Most popular</b> section
5. Verify that the <b>Most popular</b> section is context-sensitive

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that user can see the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin shows the <b>Most popular</b> section</br>- Go to any page > <b>Most popular</b> section|1) On any page, examine the <b>Most popular</b> section|1) The <b>Most popular</b> section is shown and contains three most visited articles during the configured period|

### **#2. Verify that user can see articles only for the configured period in the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configured <b>Day</b> period</br>- Go to any page > <b>Most popular</b> section|1) On any page, examine the <b>Most popular</b> section|1) The <b>Most popular</b> section is shown and contains three most visited articles on the last day|

### **#3. Verify that user can’t see the hidden Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides the <b>Most popular</b> section</br>- Go to any page where the <b>Most popular</b> section should be present|1) On any page, examine the <b>Most popular</b> section|1) The <b>Most popular</b> section is not shown|

### **#4. Verify that the user is redirected to the proper article by selecting the article in the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to any page > <b>Most popular</b> section|1) Select any article|1) The user is redirected to the article page|

### **#5. Verify that the Most popular section is context-sensitive**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Go through all pages within the <b>Most popular</b> section</br>2) Examine the <b>Most popular</b> section|2) Articles in the <b>Most popular</b> section change according to the visited page|

</details>
