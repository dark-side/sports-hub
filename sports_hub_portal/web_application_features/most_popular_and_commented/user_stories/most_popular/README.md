### Back to [The most popular/commented articles on the portal](../../) feature

# Allow site user to view the most popular articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view the Most popular section
    So that I can read articles that have the highest number of views during the period configured by admin (day, week, month, year)

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the Most popular section</i></b>

Given I a site user

When I view a page with the <b>Most popular</b> section
Then I see this section has a list with 3 most popular articles (based on page views in the configured period)
  And I see that each article has:
    - Thumbnail photo
    - Headline (on the right from the photo)
    - Caption (under Headline)

When I select an article
Then I am taken to the article page
  And the <b>Most popular section</b> is context-sensitive which means:
  - The <b>Home</b> page contains the most popular articles from the whole articles list
  - Any other page contains the most popular articles that belong to a category, subcategory, or team of the current page

When the <b>Most popular</b> section is hidden by the admin
Then I don’t see the <b>Most popular</b> section on any page where it can be present

When the <b>Most popular</b> section is shown by admin
Then I see the <b>Most popular</b> section on any page where it can be present
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Most popular</b> articles section

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Most popular articles section:**

![Users see the Most popular articles section](/sports_hub_portal/web_application_features/most_popular_and_commented/images/most_popular_commented.png)

</details>

## Test cases

1. Verify that user can see the <b>Most popular</b> section
2. Verify that user can see articles only from the configured period in the <b>Most popular</b> section
3. Verify that user can’t see the hidden <b>Most popular</b> section
4. Verify that the user is redirected to the proper article by selecting the article in the <b>Most popular</b> section
5. Verify that the <b>Most popular</b> section is context-sensitive

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that user can see the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin shows the <b>Most popular</b> section</br>- Go to the Sports Hub home page</br>- Go to any page > <b>Most popular</b> section|1) On any page, examine the <b>Most popular</b> section|1) The <b>Most popular</b> section is shown and contains three most visited articles in the configured period|

### **#2. Verify that user can see articles only from the configured period in the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin configured <b>Day</b> period</br>- Go to the Sports Hub home page</br>- Go to any page > <b>Most popular</b> section|1) On any page, examine the <b>Most popular</b> section|1) The <b>Most popular</b> section is shown and contains three most visited articles on the last day|

### **#3. Verify that user can’t see the hidden Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides the <b>Most popular</b> section</br>- Go to the Sports Hub home page</br>- Go to any page where the <b>Most popular</b> section should be present|1) On any page, examine the <b>Most popular</b> section|1) The <b>Most popular</b> section is not shown|

### **#4. Verify that the user is redirected to the proper article by selecting the article in the Most popular section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Go to any page > <b>Most popular</b> section|1) Select any article|1) The user is redirected to the article page|

### **#5. Verify that the Most popular section is context-sensitive**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page|1) Go through all pages within the <b>Most popular</b> section</br>2) Examine the <b>Most popular</b> section|2) Articles in the <b>Most popular</b> section change according to the visited page|
</details>
