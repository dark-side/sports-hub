### Back to [Home page of the portal](../../) feature

# Display the main articles for the site users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see the main articles on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the main articles section on the Home page</i></b>

Given I am a site user

When I am on the <b>Home</b> page
Then I see the main articles section at the top of the page
  And I see the carousel section that contains rotating articles that are configured by the admin (if there are more than one article)
  And I see that each article has the following information:
    - Photo
    - Headline
    - Caption
    - Category
    - The link button to the article page
  And I see the active article with large photo changes every three seconds
  And I see a numbered carousel for navigation to manually change the active article

When I click on the number in the carousel
Then I see active article changed and the carousel continues from that article

When I hover over the active article photo
Then I see the automatic rotation is paused until I move my mouse from the active article photo

When I click on any article
Then I am taken to the article view page
</pre>

## Mockups

1. User sees a Home page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees a Home page:**

![User sees a Home page](/products/sport_news_portal/web_application_features/home_page/images/home_page_user_side.png)

</details>

## Test cases

1. Verify that the Main articles section on the home page contains 5 rotating articles with all needed information
2. Verify that it is possible to select any article to be in focus
3. Verify that carousel is not present in case of only one article is configured
4. Verify that rotation of articles stops when the mouse hovers over an article photo
5. Verify that deleted article is not shown
6. Verify that the user is redirected to the right page after clicking on the article in the Main articles section

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the Main articles section on the home page contains 5 rotating articles with all needed information**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Admin configured 5 articles for the Main articles section|1) On the home page, examine the Main articles section</br>2) Wait more than 15 seconds|1) Main articles section on the home page contains 5 rotating articles</br>2) Each article contains the following information:</br>- Photo</br>- Headline</br>- Caption</br>- Category</br>- The link button to the article page</br>Each article stays active for 3 seconds. Articles rotate in a cycle|

### **#2. Verify that it is possible to select any article to be in focus**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- There are 1+ article added by the admin|1) On the Home page, examine the Main articles section</br>2) Click on any number</br>3) Wait more than 3 seconds|2) Selected article becomes the main one</br>3) Rotation of articles continues starting from the selected article|

### **#3. Verify that carousel is not present in case of only one article is configured**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- There is only 1 article added by the admin|1) On the Home page, examine the Main articles section|1) Carousel of articles is not present|

### **#4. Verify that rotation of articles stops when the mouse hovers over an article photo**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- There are 1+ article added by the admin|1) On the home page, examine the Main articles section</br>2) Hover over any article photo</br>3) Wait more than 3 seconds</br>4) Move the mouse pointer from the picture|3) The articles do not rotate</br>4) Rotation of articles is restored|

### **#5. Verify that deleted article is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin removed some article</br>- Go to Sport News home page|1) On the home page, examine the Main articles section|1) The removed article is not present|

### **#6. Verify that the user is redirected to the right page after clicking on the article in the Main articles section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page|1) On the home page, examine the Main articles section</br>2) In the Main articles section, click on any article|2) User is redirected to the right page|

</details>
