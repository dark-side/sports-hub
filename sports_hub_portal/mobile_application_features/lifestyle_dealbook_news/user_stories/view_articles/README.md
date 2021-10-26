### Back to [Lifestyle and Dealbook news](../../) feature

# Allow users to visit and read Lifestyle and Dealbook news

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to open the Lifestyle and Dealbook pages to read news

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the Lifestyle and Dealbook page</i></b>

Given I am a user

When I view the Main menu
Then I see the <b>Dealbook</b> menu item right after the <b>Lifestyle</b> menu item

When I tap the <b>Dealbook</b> or <b>Lifestyle</b> menu item
Then I am redirected to the <b>Dealbook</b> or <b>Lifestyle</b> page

When I view the <b>Dealbook</b> or <b>Lifestyle</b> page
Then I see:
  - The <b>Dealbook</b> or <b>Lifestyle</b> heading at the top of the page
  - A large photo of the most recent article in Dealbook or Lifestyle
  - Publish date
  - Article headline
  - Article metadata, including author and source
  - The <b>More</b> button
  - The list of articles located below the photo from the most recent articles including:
    - Article thumbnail photo
    - Article Headline
    - First few sentences of the article content
  - Scroll bar next to the list of articles
  - The <b>Most Popular</b> section
  - The <b>Most Commented</b> section

When I tap select any article or tap <b>More</b>
Then I am taken to the page with the article

When I scroll the list of articles
Then I see a list of articles is appended with a new portion of articles
  And I see the list of articles should be relevant to the <b>Dealbook</b> or <b>Lifestyle</b> topics

When I view the <b>Most Popular</b> section
Then I see only most viewed articles for the period configured by admin from <b>Dealbook</b> or <b>Lifestyle</b>

When I view the <b>Most Commented</b> section
Then I see only articles with biggest amount of comments for the period configured by admin from <b>Dealbook</b> or <b>Lifestyle</b>
</pre>

## Mockups

1. Users see the <b>Lifestyle</b> and <b>Dealbook</b> in the navigation menu
2. Users see the <b>Lifestyle</b> page
3. Users see the <b>Dealbook</b> page
4. Dealbook full page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Lifestyle and Dealbook in the navigation menu:**

![Users see the Lifestyle and Dealbook in the navigation menu](/sports_hub_portal/mobile_application_features/lifestyle_dealbook_news/images/application_navigation_menu.png)

**2. Users see the Lifestyle page:**

![Users see the Lifestyle page](/sports_hub_portal/mobile_application_features/lifestyle_dealbook_news/images/application_lifestyle_page.png)

**3. Users see the Dealbook page:**

![Users see the Dealbook page](/sports_hub_portal/mobile_application_features/lifestyle_dealbook_news/images/application_dealbook_page.png)

**4. Dealbook full page:**

![Dealbook full page](/sports_hub_portal/mobile_application_features/lifestyle_dealbook_news/images/dealbook_news_list.png)

</details>

## Test cases

1. Verify the most recent article is shown as the main one on the page
2. Verify redirection to the article page by tapping the <b>More</b> button for main article
3. Verify redirection to the article page by tapping the header for main article
4. Verify the list of articles on the <b>Lifestyle</b> and <b>Dealbook</b> pages
5. Verify redirection to the article page by tapping the header for article from the list
6. Verify the list of articles in the <b>Most popular</b> section on the <b>Lifestyle</b> and <b>Dealbook</b> pages
7. Verify the list of articles in the <b>Most commented</b> section on the <b>Lifestyle</b> and <b>Dealbook</b> pages

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the most recent article is shown as the main one on the page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the main article on the page|1) The main article is the most recent article from the <b>Lifestyle</b> and <b>Dealbook</b> page. It is shown as large photo with:</br>- Publish date</br>- Article headline</br>- Article metadata, including author and source</br>- The <b>More</b> button|

### **#2. Verify redirection to the article page by tapping the More button for main article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Tap the <b>More</b> button for the main article|1) The user is redirected to the appropriate article page|

### **#3. Verify redirection to the article page by tapping the header for main article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Tap the header for the main article|1) The user is redirected to the appropriate article page|

### **#4. Verify the list of articles on the Lifestyle and Dealbook pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the list of articles|1) The list of articles is formed according to the <b>Lifestyle</b> and <b>Dealbook</b>|

### **#5. Verify redirection to the article page by tapping the header for article from the list**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Tap the header for any article from the list|1) The user is redirected to the appropriate article page|

### **#6. Verify the list of articles in the Most popular section on the Lifestyle and Dealbook pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the list of articles in the <b>Most popular</b> section|1) The list of most viewed articles is formed according to the <b>Lifestyle</b> and <b>Dealbook</b> and for the period configured by admin in the <b>Most popular</b> section|

### **#7. Verify the list of articles in the Most commented section on the Lifestyle and Dealbook pages**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the <b>Lifestyle</b> and <b>Dealbook</b> page|1) Examine the list of articles in the <b>Most commented</b> section|1) The list of most commented articles is formed according to the <b>Lifestyle</b> and <b>Dealbook</b> and for the period configured by admin in the <b>Most commented</b> section|
</details>
