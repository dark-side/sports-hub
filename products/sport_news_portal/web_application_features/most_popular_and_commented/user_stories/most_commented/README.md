### Back to [Most Popular/Commented articles on the portal](../../) feature

# Allow site user to view most commented articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user 
    I want to view the Most commented section 
    So that I can read articles that have the highest number of comments in the configured by admin period (day, week, month, year)

## Acceptance criteria

<pre>
Scenario: A site user views the Most commented section
Given I am logged in as a site user

When I view a page with the <b>Most commented</b> section
Then I see this section has a list with 3 most commented articles (most commented based on the number of comments in the configured period)
  And I see that each article has:
    - Thumbnail photo
    - Headline (on the right from the photo)
    - Caption (under Headline)

When I click on an article
Then I am taken to the article page
  And the <b>Most commented</b> section is context-sensitive which means:
    - Home page – contains the most commented articles from the whole articles list
    - Any other page – contains the most commented articles that belong to a category, conference, or team, of the current page

When the <b>Most commented</b> section is hidden by admin
Then I don’t see the <b>Most commented</b> section on any page where it can be present

When the <b>Most commented</b> section is shown by admin
Then I see the <b>Most commented</b> section on any page where it can be present
</pre>

## Mockups

1. User sees most commented articles section

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees most commented articles section:**

![User sees most commented articles section](/products/sport_news_portal/web_application_features/most_popular_and_commented/images/most_popular_commented.png)

</details>

## Test cases

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that user can see the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin shows the Most commented section</br>- Go to Sport News Home page</br>- Go to any page -> <b>Most commented</b> section|1) On any page, examine the <b>Most commented</b> section|1) The <b>Most commented</b> section is shown and contains the three most visited articles in the configured period|

### **#2. Verify that user can see articles only from the configured period in the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configured <b>Day</b> period</br>- Go to Sport News Home page</br>- Go to any page -> <b>Most commented</b> section|1) On any page, examine the <b>Most commented</b> section|1) The <b>Most commented</b> section is shown and contains the three most visited articles on the last day|

### **#3. Verify that user can’t see hidden the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hide <b>Most commented</b> section</br>- Go to Sport News Home page</br>- Go to any page where the <b>Most commented</b> section should be present|1) On any page, examine the <b>Most commented</b> section|1) The <b>Most commented</b> section is not shown|

### **#4. Verify that the user is redirected to the proper article by clicking on the article in the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News Home page</br>- Go to any page -> <b>Most commented</b> section|1) Click on any article|1) User is redirected to the article page|

### **#5. Verify that the Most commented section is context-sensitive**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News Home page|1) Go through all pages with the <b>Most commented</b> section</br>2) Examine the <b>Most commented</b> section|2) Articles in the <b>Most commented</b> section change according to the visited page|
</details>
