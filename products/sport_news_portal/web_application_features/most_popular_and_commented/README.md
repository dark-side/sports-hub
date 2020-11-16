# Most Popular/Commented articles on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

When a user is viewing pages that contain the Most popular and Most commented sections, he/she should be able to see articles that have the highest number of views (Most popular) or the highest number of comments (Most commented) during the period configured by admin. The Most popular and Most commented sections should be context-sensitive:
  - Home page – contains the most popular and most commented articles from the whole articles list
  - Any other page – contains the most popular and the most commented articles that belong to the same category, conference, or team as the current page 
Admin user can show or hide the Most popular and Most commented sections for the whole site on the Home configuration page.
Admin user can configure the time period for the Most popular and Most commented sections

## Check list:

  - Verify if UI corresponds to prototype
  - Admin user should be able to show and hide the Most popular section for the whole site
  - Admin user should be able to configure the time period (Day, Weak, Month, Year) for the most popular section for the whole site
  - Admin user should be able to show and hide the Most commented section for the whole site
  - Admin user should be able to configure the time period (Day, Weak, Month, Year) for the Most commented section for the whole site
  - User should be able to see articles with the highest number of visits during configured by admin period in the Most popular section
  - User should be able to see articles with the highest number of comments during configured by admin period  in the Most commented section

## Prototype of the feature

  Please click [here](https://www.figma.com/proto/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=0%3A1074&scaling=min-zoom) to see a clickable prototype for the feature as an admin user and [here](https://www.figma.com/proto/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=0%3A2&scaling=min-zoom) to see prototype for the feature as a site user.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure the Most popular section**](/products/sport_news_portal/web_application_features/most_popular_and_commented/user_stories/most_popular_configuration)|<pre>As an admin user<br>I want to configure the Most popular section</pre>
2 |[**Allow admin user to configure the Most commented section**](/products/sport_news_portal/web_application_features/most_popular_and_commented/user_stories/most_commented_configuration)|<pre>As an admin user<br>I want to configure the Most commented section</pre>
3 |[**Allow site user to view the most popular articles**](/products/sport_news_portal/web_application_features/most_popular_and_commented/user_stories/most_popular)|<pre>As a site user<br>I want to view a Most popular block<br>So that I can read articles that have the highest number of views in the configured by admin period (day, week, month, year)</pre>
4 |[**Allow site user to view most commented articles**](/products/sport_news_portal/web_application_features/most_popular_and_commented/user_stories/most_commented)|<pre>As a site user<br>I want to view a Most commented block<br>So that I can read articles that have the highest number of comments in the configured by admin period (day, week, month, year)</pre>
