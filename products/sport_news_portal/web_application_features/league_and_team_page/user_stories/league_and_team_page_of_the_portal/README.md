### Back to [League and Team Page of the portal](/../../) feature

# Allow users to view League/Team Page of the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test Scenarios](#test-scenarios)

## Description

    As a site user
    I want to able be to open League or Team page
    So that I can view articles that are related to selected League or Team

## Acceptance criteria

    Scenario: A site user views the League or Team page
    Given I am logged in as a site user

    When I view League or Team page
    Then I see: 
      - Heading at the top of the page that contains the path to the page (example: NBA\AFC South\Tennessee)
      - Big photo from the most recent article in the selected Team or League with the square on the right side of the photo that contains:
        - Article headline 
        - Article metadata (including author and source)
        - More button in the left-bottom corner
      - The list of articles (the number of articles to show can be specified in the CMS) located below the photo from the most recent article including: 
        - Article thumbnail photo in the left side
        - Article Headline to the right from the photo
        - First few sentences of the article content 
      - Scroll bar next to the list of articles
    When I click on any article or click on More button
    Then I am taken to the page containing the article
    When I scroll the list of the articles
    Then I see a the list of articles increases 
    And I see the list of articles should be relevant to the selected Team or League topics
    And I see the number of articles that appear in the list should be defined in the CMS
    
## Mockups

1. User sees League page
2. User sees Team page

<details>
  <summary>Click here to see mockups details</summary>

**1. User sees League page:**

![League Page Screen](/products/sport_news_portal/web_application_features/league_and_team_page/images/league_page.png)

**2. User sees Team page:**

![Team Page Screen](/products/sport_news_portal/web_application_features/league_and_team_page/images/team_page.png)

</details>

## Test Scenarios

1. Verify navigating to the team/league page from the sidebar menu
2. Verify the content of the information square on the team/league page
3. Verify the list of articles on the team/league page
4. Verify navigating to the article’s page after clicking on more button
5. Verify the scroll bar functionality on the team/league page

<details>
  <summary>Click here to see test scenarios details</summary>

### **#1. Verify navigating to the team/league page from the sidebar menu**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|
|4|Click on Sport category (NBA)|Combo-box with subcategories appears
|5|Click on subcategory (AFC South)|Combo-box with teams appears
|6|Click on a team (Tennessee)|User is navigated to the Tennesse Team page

### **#2. Verify the content of the information square on the team/league page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|
|4|Click on Sport category (NBA)|Combo-box with subcategories appears
|5|Click on subcategory (AFC South)|Combo-box with teams appears
|6|Click on a team (Tennessee)|User is navigated to the Tennesse Team page
|7|Observe the content of the square on the right side of the photo|The square contains:<br>- Article headline<br>- Article metadata (including author and source)<br>- More button in the left-bottom corner

### **#3. Verify the list of articles on the team/league page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|
|4|Click on Sport category (NBA)|Combo-box with subcategories appears
|5|Click on subcategory (AFC South)|Combo-box with teams appears
|6|Click on a team (Tennessee)|User is navigated to the Tennesse Team page
|7|Observe the list of articles located below the photo from the most recent article|The list of articles includes:<br>- Article thumbnail photo in the left side<br>- Article Headline to the right from the photo<br>- First few sentences of the article content<br>The list of articles should be relevant to the selected Team or League topics

### **#4. Verify navigating to the article’s page after clicking on more button**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|
|4|Click on Sport category (NBA)|Combo-box with subcategories appears
|5|Click on subcategory (AFC South)|Combo-box with teams appears
|6|Click on a team (Tennessee)|User is navigated to the Tennesse Team page
|7|Click on More button in the square on the right side of the photo|User is navigating to the page containing the article

### **#5. Verify the scroll bar functionality on the team/league page**

|#|Steps|Expected Result
------|-------|----------
|1|Go to the sport news site|
|2|Log in your user account|
|3|Observe sidebar menu|
|4|Click on Sport category (NBA)|Combo-box with subcategories appears
|5|Click on subcategory (AFC South)|Combo-box with teams appears
|6|Click on a team (Tennessee)|User is navigated to the Tennesse Team page
|7|Scroll the list of the articles on the team page|The list of articles will be increased 

</details>
