### Back to [The most popular/commented articles on the portal](../../) feature

# Allow site users to view the most commented articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view the Most commented section
    So that I can read articles that have the highest number of comments during the period configured by admin (day, week, month, year)

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the Most commented section</i></b>

Given I am logged in as a site user

When I view a page with the <b>Most commented</b> section
Then I see this section has a list with 3 most commented articles (based on the number of comments in the configured period)
  And I see that each article has:
    - Thumbnail photo
    - Headline (on the right from the photo)
    - Caption (under Headline)

When I select an article
Then I am taken to the article page
  And the <b>Most commented</b> section is context-sensitive which means:
    - The <b>Home</b> page contains the most commented articles from the whole articles list
    - Any other page contains the most commented articles that belong to a category, conference, or team of the current page

When the <b>Most commented</b> section is hidden by admin
Then I don’t see the <b>Most commented</b> section on any page where it can be present

When the <b>Most commented</b> section is shown by admin
Then I see the <b>Most commented</b> section on any page where it can be present
</pre>

## Mockups

1. Users see the <b>Most commented</b> articles section

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Most commented articles section:**

![Users see the Most commented articles section](/products/sports_hub_portal/web_application_features/most_popular_and_commented/images/most_popular_commented.png)

</details>

## Test cases

1. Verify that users can see the <b>Most commented</b> section
2. Verify that users can see articles only from the configured period in the <b>Most commented</b> section
3. Verify that users can’t see the hidden <b>Most commented</b> section
4. Verify that users are redirected to the proper article by selecting the article in the <b>Most commented</b> section
5. Verify that the <b>Most commented</b> section is context-sensitive

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that users can see the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin shows the <b>Most commented</b> section</br>- Go to the Sports Hub home page</br>- Go to any page > <b>Most commented</b> section|1) On any page, examine the <b>Most commented</b> section|1) The <b>Most commented</b> section is shown and contains three most visited articles in the configured period|

### **#2. Verify that users can see articles only from the configured period in the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configured <b>Day</b> period</br>- Go to the Sports Hub home page</br>- Go to any page > <b>Most commented</b> section|1) On any page, examine the <b>Most commented</b> section|1) The <b>Most commented</b> section is shown and contains three most visited articles on the last day|

### **#3. Verify that users can’t see the hidden Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides <b>Most commented</b> section</br>- Go to the Sports Hub home page</br>- Go to any page where the <b>Most commented</b> section should be present|1) On any page, examine the <b>Most commented</b> section|1) The <b>Most commented</b> section is not shown|

### **#4. Verify that users are redirected to the proper article by selecting the article in the Most commented section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Go to any page > <b>Most commented</b> section|1) Select any article|1) The user is redirected to the article page|

### **#5. Verify that the Most commented section is context-sensitive**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page|1) Go through all pages within the <b>Most commented</b> section</br>2) Examine the <b>Most commented</b> section|2) Articles in the <b>Most commented</b> section change according to the visited page|
</details>
