### Back to [View articles in the application](../../) feature

# Allow users to view league/team page in the application

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As a user
    I want to be able to open the league or team page
    So that I can view articles that are related to selected league or team

## Acceptance criteria
<pre>
<b><i>Scenario: A user views the league or team page</i></b>

Given I am a user

When I view the league or team page
Then I see:
  - Heading at the top of the page that contains the path to the page (example: NBA\AFC South\Tennessee)
  - Big photo from the most recent article in the selected team or league
  - Article headline
  - Article metadata (including author and source)
  - The <b>More</b> button
  - The list of articles located below the photo from the most recent article including:
    - Article thumbnail photo in the left side
    - Article Headline to the right from the photo
    - First few sentences of the article content
  - Scroll bar next to the list of articles

When I tap any article or tap <b>More</b>
Then I am taken to the page containing the article

When I scroll the list of the articles
Then I see the list of articles increases
  And I see the list of articles should be relevant to the selected team or league topics
</pre>

## Mockups

1. Users see a list of leagues on the menu
2. The league related (NBA) articles list
3. Users see a list of leagues, confereces, and teams on the menu
4. Users see the article page
5. Article full page

<details>
  <summary>Click here to see mockups details</summary>

**1. Users see a list of leagues on the menu:**

![Users see a list of leagues on the menu](/sports_hub_portal/mobile_application_features/articles_view/images/application_menu_league_list.png)

**2. The league related (NBA) articles list:**

![The league related (NBA) articles list](/sports_hub_portal/mobile_application_features/articles_view/images/league_articles_page.png)

**3. Users see a list of leagues, confereces, and teams on the menu:**

![Users see a list of leagues, confereces, and teams on the menu](/sports_hub_portal/mobile_application_features/articles_view/images/application_menu_full_list.png)

**4. Users see the article page:**

![Users see the article page](/sports_hub_portal/mobile_application_features/articles_view/images/application_article_page.png)

**5. Article full page:**

![Article full page](/sports_hub_portal/mobile_application_features/articles_view/images/article_page.png)

</details>

## Test cases

1. Verify navigating to the team and league page from the main menu
2. Verify the list of articles on the team/league page
3. Verify redirection to the article page by tapping the <b>More</b> button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify navigating to the team and league page from the main menu**

|Preconditions|Steps|Expected result
--------------|-----|----------
||1) Examine the main menu</br>2) Tap the sports category (NBA)</br>3) Tap the subcategory (AFC South)</br>4) Tap a team (Tennessee)|2) Submenu with subcategories opens</br>3) Submenu with teams opens</br>4) The user is redirected to the Tennessee team page|

### **#2. Verify the list of articles on the team/league page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|The user is on the team page|1) Examine the list of articles|1) The list of articles is relevant to the selected team|

### **#3. Verify redirection to the article page by tapping the More button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- The user is on the team page|1) Tap the More button in the main article section|1) The user is redirected to the article page|
</details>
