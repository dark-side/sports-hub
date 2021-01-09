### Back to [Home page of the portal](../../) feature

# Display the Breakdown block for the site users on the Home page

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to see the Breakdown section on the Home page

## Acceptance criteria

<pre>
<b><i>Scenario: A site user views the Breakdown section on the home page</i></b>

Given I am a site user

When I am on the <b>Home</b> page
Then I see a <b>Breakdown</b> section after the main articles
  And I see the section contains the heading <b>Breakdown</b>
  And I see 4 newest articles for the category are formed into a group
  And I see for each article: 
    - Photo
    - Headline
    - Caption - for the 3 secondary articles

When the <b>Conference</b> is selected by the admin
Then I see only news from this conference

When the <b>Team</b> is selected by the admin
Then I see only news from this team

When the <b>Breakdown</b> section is hidden by the admin
Then I do not see the <b>Breakdown</b> section

When the <b>Breakdown</b> section is shown by admin
Then I see the <b>Breakdown</b> section

When some breakdown is deleted from the <b>Breakdown</b> section
Then I do not see it anymore in the <b>Breakdown</b> section

When I click on any of the article photos, headlines, or captions in the <b>Breakdown</b> section
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

1. Verify that 4 newest articles from the category for the configured breakdown are shown for the user
2. Verify that 4 newest articles from the conference for the configured breakdown are shown for the user
3. Verify that 4 newest articles from the team for the configured breakdown are shown for the user
4. Verify that the user is redirected to the right page by clicking on the article photo, headline, or caption in the Breakdow
5. Verify that deleted breakdown is not shown
6. Verify that the hidden Breakdown section is not shown
7. Verify that unhidden Breakdown section is shown

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that 4 newest articles from the category for the configured breakdown are shown for the user**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Home page -> <b>Breakdown</b> section</br>- There is breakdown configured for category (conference and team are not selected)|1) Examine the <b>Breakdown</b> section|1) There is a <b>Breakdown</b> of 4 newest articles according to the selected category|

### **#2. Verify that 4 newest articles from the conference for the configured breakdown are shown for the user**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Home page -> <b>Breakdown</b> section</br>- There is a breakdown configured for the conference (Team is not selected)|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected conference|

### **#3. Verify that 4 newest articles from the team for the configured breakdown are shown for the user**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Home page -> <b>Breakdown</b> section</br>- There is a breakdown configured for a team|1) Examine the <b>Breakdown</b> section|1) There is a breakdown of 4 newest articles according to the selected team|

### **#4. Verify that the user is redirected to the right page by clicking on the article photo, headline, or caption in the Breakdown section**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to the Home page -> <b>Breakdown</b> section|1) Click on any article photo</br>2) Click on any headline</br>3) Click on any caption|1) User is redirected to the article page</br>2) User is redirected to the article page</br>3) User is redirected to the article page|

### **#5. Verify that deleted breakdown is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin removed some breakdown</br>- Go to the Home page -> <b>Breakdown</b> section|1) On the home page, examine the <b>Breakdown</b> section|1) The removed breakdown is not present|

### **#6. Verify that the hidden Breakdown section is not shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin hides <b>Breakdown</b> section</br>- Go to Sport News Home page|1) On the home page, examine the <b>Breakdown</b> section|1) The <b>Breakdown</b> section is not present|

### **#7. Verify that unhidden Breakdown section is shown**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Admin shows <b>Breakdown</b> section</br>- Go to Sport News Home page|1) On the home page, examine the <b>Breakdown</b> section|1) The <b>Breakdown</b> section is present|

</details>
