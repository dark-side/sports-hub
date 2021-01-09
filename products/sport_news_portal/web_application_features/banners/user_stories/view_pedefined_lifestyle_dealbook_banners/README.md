### Back to [Banners on the portal](../../) feature

# Allow site users to view predefined Lifestyle and Dealbook banners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to view predefined Lifestyle and Dealbook banners on the portal

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views Lifestyle and Dealbook banners in the sidebar section</i></b>

Given I am a site user

When I view any page with the <b>Lifestyle</b> and <b>Dealbook</b> banners in the sidebar section
Then I see they contain the most recent articles
  And I see the following:
    - Heading <b>Lifestyle</b> / <b>Dealbook</b>
    - Article Photo
    - Article header

When I click the article header
Then I am taken to the appropriate article page
</pre>

## Mockups

1. User sees Dealbook banner in the sidebar section

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees Dealbook banner in the sidebar section:**

![User sees Dealbook banner in the sidebar section](/products/sport_news_portal/web_application_features/banners/images/banners_user_side.png)

</details>

## Test cases

1. Verify the content of the Lifestyle banner on the right side
2. Verify redirection to the appropriate article page by click on the header for the article from the Lifestyle banner
3. Verify the content of the Dealbook banner on the right side
4. Verify redirection to the appropriate article page by click on the header for the article from the Dealbook banner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Lifestyle banner on the right side**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- <b>Lifestyle</b> banner is enabled|1) Examine the <b>Lifestyle</b> banner on the right side|1) The <b>Lifestyle</b> banner contains the most recent lifestyle article and the following:</br>- Heading <b>Lifestyle</b></br>- Article Photo</br>- Article header|

### **#2. Verify redirection to the appropriate article page by click on the header for the article from the Lifestyle banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- <b>Lifestyle</b> banner is enabled|1) Click the header for the <b>Lifestyle</b> banner article|1) The user is redirected to the appropriate article page|

### **#3. Verify the content of the Dealbook banner on the right side**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- <b>Dealbook</b> banner is enabled|1) Examine the <b>Dealbook</b> banner on the right side|1) The <b>Dealbook</b> banner contains the most recent dealbook article and the following:</br>- Heading <b>Dealbook</b></br>- Article Photo</br>- Article header|

### **#4. Verify redirection to the appropriate article page by click on the header for the article from the Dealbook banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- <b>Dealbook</b> banner is enabled|1) Click the header for the <b>Dealbook</b> banner article|1) The user is redirected to the appropriate article page|

</details>
