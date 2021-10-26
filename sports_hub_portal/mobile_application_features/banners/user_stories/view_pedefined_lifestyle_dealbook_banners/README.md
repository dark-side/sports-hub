### Back to [Banners in the application](../../) feature

# Allow users to view predefined Lifestyle and Dealbook banners in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to view predefined Lifestyle and Dealbook banners in the application
    So that I can quickly view the most recent lifestyle and dealbook articles

## Acceptance criteria

<pre>
<b><i>Scenario: A user views Lifestyle and Dealbook banners</i></b>

Given I am a user

When I view any page with the <b>Lifestyle</b> or <b>Dealbook</b> banners
Then I see they contain the most recent articles from <b>Lifestyle</b> or <b>Dealbook</b>
  And I see the following:
    - Heading <b>Lifestyle</b> or <b>Dealbook</b>
    - Article Photo
    - Article header

When I tap the article header
Then I am taken to the appropriate article page
  And I see it is the most recent <b>Lifestyle</b> or <b>Dealbook</b> article page
</pre>

## Mockups

1. Users see the <b>Dealbook</b> banner at the bottom of the page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Dealbook banner at the bottom of the pagen:**

![Users see the Dealbook banner in the sidebar section](/products/sports_hub_portal/mobile_application_features/banners/images/application_dealbook_banner.png)

</details>

## Test cases

1. Verify the content of the <b>Lifestyle</b> banner
2. Verify redirection to the appropriate article page by tapping the header for article from the <b>Lifestyle</b> banner
3. Verify that there is the most recent article shown in the <b>Lifestyle</b> banner
4. Verify the content of <b>Dealbook</b> banner
5. Verify redirection to the appropriate article page by tapping the header for the article from the <b>Dealbook</b> banner
6. Verify that there is the most recent article shown in the <b>Dealbook</b> banner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the Lifestyle banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Lifestyle</b> banner is enabled|1) Examine the Lifestyle banner after the main page content|1) The Lifestyle banner contains:</br>- Heading <b>Lifestyle</b></br>- Article photo</br>- Article header|

### **#2. Verify redirection to the appropriate article page by tapping the header for the article from the Lifestyle banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Lifestyle</b> banner is enabled</br>- The user is on any page|1) Tap the header for the <b>Lifestyle</b> banner article|1) The user is redirected to the appropriate article page|

### **#3. Verify that there is the most recent article shown in the Lifestyle banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Lifestyle</b> banner is enabled</br>- The user is on any page|1) Examine the <b>Lifestyle</b> banner|1) The <b>Lifestyle</b> banner contains the most recent article from the <b>Lifestyle</b> articles|

### **#4. Verify the content of Dealbook banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Dealbook</b> banner is enabled|1) Examine the <b>Dealbook</b> banner after the main page content|1) The <b>Dealbook</b> banner contains:</br>- Heading <b>Dealbook</b></br>- Article photo</br>- Article header|

### **#5. Verify redirection to the appropriate article page by tapping the header for the article from the Dealbook banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Dealbook</b> banner is enabled</br>- The user is on any page|1) Tap the header for the <b>Dealbook</b> banner article|1) The user is redirected to the appropriate article page|

### **#6. Verify that there is the most recent article shown in the Dealbook banner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The <b>Dealbook</b> banner is enabled</br>- The user is on any page|1) Examine the <b>Dealbook</b> banner|1) The <b>Dealbook</b> banner contains the most recent article from the <b>Dealbook</b> articles|
</details>
