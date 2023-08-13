### Back to [Home page of the portal](../../README.md) feature

# Display the Main articles section for site users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see the Main articles section on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the Main articles section on the Home page</i></b>

Given I am a site user

When I am on the <b>Home</b> page
Then I see the <b>Main articles</b> section at the top of the page
  And I see the carousel section that contains rotating articles that are configured by admin (if there are more than one article)
  And I see that each article has the following information:
    - Photo
    - Headline
    - Caption
    - Category
    - The link button to the article page
  And I see the active article with large photo changes every three seconds
  And I see a numbered carousel for navigation to manually change the active article

When I select the number in the carousel
Then I see active article changed and the carousel continues from that article

When I hover over the active article photo
Then I see the automatic rotation is paused until I move my mouse from the active article photo

When I select any article
Then I am taken to the article view page
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Users see the <b>Home</b> page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the Home page:**

![Users see the Home page](/sports_hub_portal/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test cases

1. Verify that the <b>Main articles</b> section on the <b>Home</b> page contains 5 rotating articles with all needed information
2. Verify that it is possible to select any article to be in focus
3. Verify that carousel is not present in case of only one article is configured
4. Verify that rotation of articles stops when the mouse hovers over an article photo
5. Verify that the deleted article is not shown
6. Verify that the user is redirected to the right page after selecting the article in the <b>Main articles</b> section

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Main articles section on the Home page contains 5 rotating articles with all needed information**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- Admin configured 5 articles for the <b>Main articles</b> section|1) On the <b>Home</b> page, examine the <b>Main articles</b> section</br>2) Wait more than 15 seconds|1) <b>Main articles</b> section on the <b>Home</b> page contains 5 rotating articles</br>2) Each article contains the following information:</br>- Photo</br>- Headline</br>- Caption</br>- Category</br>- The link button to the article page</br>Each article stays active for 3 seconds. Articles rotate in a cycle|

### **#2. Verify that it is possible to select any article to be in focus**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- There are 1+ article added by admin|1) On the <b>Home</b> page, examine the <b>Main articles</b> section</br>2) Select any number</br>3) Wait more than 3 seconds|2) The selected article becomes the main one</br>3) Rotation of articles continues starting from the selected article|

### **#3. Verify that carousel is not present in case of only one article is configured**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- There is only 1 article added by admin|1) On the <b>Home</b> page, examine the <b>Main articles</b> section|1) Carousel of articles is not present|

### **#4. Verify that rotation of articles stops when the mouse hovers over an article photo**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page</br>- There are 1+ article added by admin|1) On the <b>Home</b> page, examine the <b>Main articles</b> section</br>2) Hover over any article photo</br>3) Wait more than 3 seconds</br>4) Move the mouse pointer from the picture|3) The articles do not rotate</br>4) Rotation of articles is restored|

### **#5. Verify that the deleted article is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin removed some article</br>- Go to the Sports Hub home page|1) On the <b>Home</b> page, examine the <b>Main articles</b> section|1) The removed article is not present|

### **#6. Verify that the user is redirected to the right page after selecting the article in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Sports Hub home page|1) On the <b>Home</b> page, examine the <b>Main articles</b> section</br>2) In the <b>Main articles</b> section, select any article|2) The user is redirected to the right page|

</details>
