### Back to [Lifestyle and Dealbook news](../../) feature

# Allow site users to visit and read Lifestyle and Dealbook news

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to be able to open the Lifestyle and Dealbook pages to read news

## Acceptance criteria

<pre>
<b><i>Scenario: A user visits the Lifestyle and Dealbook page</i></b>

Given I am a site user

When I view the navigation menu
Then I see the <b>Lifestyle</b> and <b>Dealbook</b> menu items

When I click the <b>Lifestyle</b> or <b>Dealbook</b> menu item
Then I am redirected to the <b>Lifestyle</b> or <b>Dealbook</b> page

When I view the <b>Lifestyle</b> or <b>Dealbook</b> page
Then I see:
  - The <b>Lifestyle</b> or <b>Dealbook</b> heading at the top of the page
  - A large photo of the most recent article in the <b>Lifestyle</b> or <b>Dealbook</b> category with the square on the right side of the photo that contains:
    - Publish date
    - Article headline
    - Article metadata including author and source
    - The <b>More</b> button in the lower-left corner
  - The list of articles located below the photo from the most recent article including: 
    - Article thumbnail photo on the left
    - Article headline on the right of the photo
    - First few sentences of the article content
  - Scroll bar next to the list of articles
  - <b>Most popular</b> section
  - <b>Most commented</b> section

When I click on any article or click <b>More</b>
Then I am taken to the page with the article

When I scroll the list of articles
Then I see a list of articles is appended with a new portion of articles
  And I see the list of articles should be relevant to the <b>Lifestyle</b> or <b>Dealbook</b> topics

When I view the <b>Most popular</b> section
Then I see only the most viewed articles for configured by admin period from the <b>Lifestyle</b> or <b>Dealbook</b>

When I view the <b>Most commented</b> section
Then I see only articles with the biggest amount of comments for configured by admin period from the <b>Lifestyle</b>
</pre>

## Mockups

1. Users see the <b>Lifestyle</b> page
1. Users see the <b>Dealbook</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Lifestyle page:**

![Users see the Lifestyle page](/products/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/lifestyle_user_page.png)

**2. Users see the Dealbook page:**

![Users see the Dealbook page](/products/sports_hub_portal/web_application_features/lifestyle_dealbook_news/images/dealbook_user_page.png)

</details>

## Test cases

1. Verify the most recent article is shown as the main one on the page
2. Verify redirection to the article page by clicking the <b>More</b> button for main article
3. Verify redirection to the article page by clicking the header for main article
4. Verify the list of articles on the <b>Lifestyle</b> and <b>Dealbook</b> pages
5. Verify redirection to the article page by clicking the header for article from the list
6. Verify the list of articles in the <b>Most popular</b> section on the <b>Lifestyle</b> and <b>Dealbook</b> pages
7. Verify the list of articles in the <b>Most commented</b> section on the <b>Lifestyle</b> and <b>Dealbook</b> pages

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the most recent article is shown as the main one on the page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the main article on the page|1) The main article is the most recent article from the <b>Lifestyle</b> and <b>Dealbook</b> page. It is shown as large photo with the square on the right side of the photo that contains publish date, article headline, article metadata including author and source, the <b>More</b> button in the lower-left corner|

### **#2. Verify redirection to the article page by clicking the More button for main article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Click the <b>More</b> button for the main article|1) The user is redirected to the appropriate article page|

### **#3. Verify redirection to the article page by clicking the header for main article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Click the header for the main article|1) The user is redirected to the appropriate article page|

### **#4. Verify the list of articles on the Lifestyle and Dealbook pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the list of articles|1) The list of articles is formed according to the <b>Lifestyle</b> and <b>Dealbook</b>|

### **#5. Verify redirection to the article page by clicking the header for article from the list**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Click the header for any article from the list|1) The user is redirected to the appropriate article page|

### **#6. Verify the list of articles in the Most popular section on the Lifestyle and Dealbook pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the list of articles in the <b>Most popular</b> section|1) The list of most viewed articles is formed according to the <b>Lifestyle</b> and <b>Dealbook</b> and for the period configured by admin in the <b>Most popular</b> section|

### **#7. Verify the list of articles in the Most commented section on the Lifestyle and Dealbook pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the list of articles in the <b>Most commented</b> section|1) The list of most commented articles is formed according to the <b>Lifestyle</b> and <b>Dealbook</b> and for the period configured by admin in the <b>Most commented</b> section|
</details>
