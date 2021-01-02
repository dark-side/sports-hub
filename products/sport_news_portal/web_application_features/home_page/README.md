# Home page of the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

When users visit our site, they should see the main page by default. The main page is called Home in the navigation menu. This page should contain the most recent news and topics, and consist of the following page sections:
  - Main articles: Admin can add at least 1 and up to 5 articles to the section. These articles will be rotating every 3 seconds. This section needs to be always present and users can not hide it from the page. Users can click on the article number to make a rotation to it. Rotation will continue from this article. The section is always present and can not be hidden.
  - Breakdown: Admin can show or hide this section on the page. The Breakdown section has to consist of breakdowns with 2-4 articles. 
Admin user can show and hide the following sections:
  - Photo of the day
  - Most popular
  - Most commented
We want to allow the admin user to configure this page, post articles, photos, and make some parts of the page visible or nonvisible.
The Most popular and Most commented functionality is described in [the separate feature](/products/sport_news_portal/web_application_features/home_page/user_stories/most_popular_and_commented).

## Check list:

  - Verify if UI corresponds to prototype
  - User should be able to see the Main articles section on the home page
  - User should be able to view the Photo of the day section on the home page
  - User should be able to see the Breakdown section on the home page
  - User should be able to navigate to another page of the site on the home page
  - Admin user shouldn’t be able to hide the Main articles section for users
  - Admin user should be able to set up the Breakdown section for a specific category
  - Admin user should be able to show and hide the Breakdown section from users
  - Admin user should be able to configure the Photo of the day section for users
  - Admin user should be able to show and hide the Photo of the day section for users

## Prototype of the feature

  Please click [here](https://www.figma.com/file/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=4523%3A10122) to see a clickable prototype for the feature.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure main articles block**](/products/sport_news_portal/web_application_features/home_page/user_stories/configuration_of_main_articles_block)|<pre>As an admin user<br>I want to set up up to 5 main articles<br>So that the site users can see them on the home page</pre>
2 |[**Display the main articles for the site users on the Home page**](/products/sport_news_portal/web_application_features/home_page/user_stories/display_main_articles_for_user)|<pre>As a site user<br>I want to see the main articles on the Home page</pre>
3 |[**Allow admin user to configure a breakdown block**](/products/sport_news_portal/web_application_features/home_page/user_stories/configuration_of_breakdown_block)|<pre>As an admin user<br>I want to set up Breakdown section news for a specific category<br>So that the site users can see them on the home page</pre>
4 |[**Display the Breakdown block for the site users on the Home page**](/products/sport_news_portal/web_application_features/home_page/user_stories/display_breakdown_for_user)|<pre>As a site user<br>I want to see the Breakdown section on the Home page</pre>
5 |[**Allow admin user to configure Photo of the Day block**](/products/sport_news_portal/web_application_features/home_page/user_stories/configuration_of_photo_of_the_day_block)|<pre>As an admin user<br>I want to be able to set up Photo of the day<br>So that the site users can see it on the Home page</pre>
6 |[**Display the Photo of the Day for the site users on the Home page**](/products/sport_news_portal/web_application_features/home_page/user_stories/display_photo_of_the_day_for_user)|<pre>As a site user<br>I want to see the Photo of the day on the Home page</pre>
7 |[**Allow admin user to preview the Home page**](/products/sport_news_portal/web_application_features/home_page/user_stories/home_page_preview)|<pre>As an admin user<br>I want to be able to preview Home page while configuration<br>So that I could review the page as a site user</pre>
