### Back to [Home page in the application](../../) feature

# Display the Main articles section for users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to see the Main articles section on the page

## Acceptance criteria

<pre>
<b><i>Scenario: A user views the Main articles section on the Home page</i></b>

Given I am an user

When I am on the <b>Home</b> page
Then I see the <b>Main articles</b> section at the top of the page
  And I see that first article is on the top and has the following information:
    - Photo
    - Publish date
    - Headline
    - First few sentences of the article content
    - The <b>More</b> button to the article page
  And I see that the rest articles have the following information:
    - Photo
    - Headline
    - First few sentences of the article content

When I select any article or tap <b>More</b>
Then I am taken to the page with the article
</pre>

## Mockups

1. Full <b>Home</b> page
2. Users see <b>Main articles</b>

<details>
  <summary>Click here to see mockups details</summary>

**1. Full Home page:**

![Full Home page](/products/sports_hub_portal/mobile_application_features/home_page/images/home_page.png)

**2. Users see Main articles**

![Users see Main articles](/products/sports_hub_portal/mobile_application_features/home_page/images/application_main_articles_section.png)

</details>

## Test cases

1. Verify that the <b>Main articles</b> section on the <b>Home</b> page contains up to 5 articles with all needed information
2. Verify that the user is redirected to the right page after selecting the article in the <b>Main articles</b> section

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Main articles section on the Home page contains up to 5 articles with all needed information**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the <b>Home</b> page</br>- Admin configured 5 articles for the <b>Main articles</b> section|1) On the <b>Home</b> page, examine the <b>Main articles</b> section|1) Main articles section on the <b>Home</b> page contains 5 articles. First article contains the following information:</br>- Photo</br>- Publish date</br>- Headline</br>- First few sentences of the article content</br>- The <b>More</b> button to the article page</br>All the rest articles contain the following information:</br>- Photo</br>- Headline</br>- First few sentences of the article content|

### **#2. Verify that the user is redirected to the right page after selecting the article in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the the <b>Home</b> page|1) On the <b>Home</b> page, examine the <b>Main articles</b> section</br>2) In the <b>Main articles</b> section, select any article|2) The user is redirected to the right page|

</details>
