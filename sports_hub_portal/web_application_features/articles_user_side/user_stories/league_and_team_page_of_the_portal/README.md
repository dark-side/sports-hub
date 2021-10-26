### Back to [Articles - user side on the portal](../../) feature

# Allow users to view league/team page of the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a site user
    I want to able be to open the league or team page
    So that I can view articles that are related to the selected league or team

## Acceptance criteria
<pre>
<b><i>Scenario: A site user views the league or team page</i></b>

Given I am a site user

When I view the league or team page
Then I see:
  - Heading at the top of the page that contains the path to the page (example: NBA\AFC South\Tennessee)
  - Big photo from the most recent article in the selected league or team with the square on the right side of the photo that contains:
    1. Article headline
    2. Article metadata (including author and source)
    3. The <b>More</b> button in the lower-left corner
  - The list of articles (the number of articles to show can be specified in the CMS) located below the photo from the most recent article including:
    1. Article thumbnail photo in the left side
    2. Article headline to the right from the photo
    3. First few sentences of the article content
  - Scroll bar next to the list of articles

When I click any article or click <b>More</b>
Then I am taken to the page containing the article

When I scroll the list of the articles
Then I see the list of articles increases
  And I see the list of articles should be relevant to the selected league or team topics
  And I see the number of articles that appear in the list should be defined in the CMS
</pre>

## Mockups

1. Users see the league related to the article page
2. Users see the team related to the article page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see the league related to the article page:**

![Users see the league related to the article page](/products/sports_hub_portal/web_application_features/articles_user_side/images/league_page.png)

**2. Users see the team related to the article page:**

![Users see the team related to the article page](/products/sports_hub_portal/web_application_features/articles_user_side/images/team_page.png)

</details>

## Test cases

1. Verify navigating to the team and league pages from the sidebar menu
2. Verify the list of articles on the team/league page
3. Verify redirection to the article page by clicking the <b>More</b> button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify navigating to the team and league pages from the sidebar menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Examine the main menu</br>2) Select the sports category (NBA)</br>3) Select the subcategory (AFC South)</br>4) Select a team (Tennessee)|2) Submenu with subcategories opens</br>3) Submenu with teams opens</br>4) The user is redirected to the Tennessee team page|

### **#2. Verify the list of articles on the team/league page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|The user is on the team page|1) Examine the list of articles|1) The list of articles is relevant to the selected team|

### **#3. Verify redirection to the article page by clicking the More button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|The user is on the team page|1) Click **More** in the main article section|1) The user is redirected to the article page|

</details>
