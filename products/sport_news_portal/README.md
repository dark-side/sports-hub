# Sports Hub portal

- [Problem](#problem)
- [Solution](#solution)
- [Goals and objectives](#goals-and-objectives)
- [User personas](#user-personas)
- [Requirements](#requirements)
  - [Functional requirements](#functional-requirements)
  - [Non-Functional requirements](#non-functional-requirements)
  - [Layout requirements](#layout-requirements)
- [User interface](#user-interface)
- [Audience](#audience)
- [Future work](#future-work)

## Problem

These days in the world filled with different kinds of news presented on various websites it’s rather hard and time consuming to find the information we need. When it comes to sports, fans spend a fair amount of time browsing the web in order to find hot news relevant to their best-loved kind of sports or their favorite league or team.

## Solution

Creating a sports news site focused exclusively on the sports activities will allow users to effectively manage the news they want to see thus helping fans and people interested in sports to address the issue of information overdose on the web and save time when looking for the news consistent with their interests.

## Goals and objectives

Specific goals are:
1. To create a web-application allowing users:
  - to read news related to different kinds of sports
  - to subscribe to the sports news of their choice
  - to receive the newsletters via email
  - to manage the kind of news they want to see (e.g. news related to the specific kind of sports,league or team)

2. To create the Content Management System (CMS) allowing users with proper permission to define the structure and content of the web-application

## User personas

**Unauthorized website user (not logged in to the Sports Hub site)**

    Available actions
      - View sports news (note: the structure of the news pages and the content of the pages (articles) are defined in the CMS)
      - Subscribe to receive sports news (note: there are a few different subscription types: General news, League news, Team news)
      - Share the news via the Social Media (when configured in the CMS)
      - Login/Sign up to the Sports Hub site (including the Login/Sign up with the Social Networks if enabled in CMS)

**Authorised website user (logged in to the Sports Hub site)**

    Available actions:
      - Manage personal info
      - Manage team subscriptions
      - Manage surveys
      - Answer the surveys
      - Comment on an article
      - Actions available for an unauthorized user

**Website Admin**

    Available actions:
    Can configure the following parts of the site via the CMS:
      - Site footer
      - Site menu (including nested menu dropdowns)
      - Site users
      - Structure of the pages
      - Articles
      - Sports Categories (Leagues)
      - Sports Conferences
      - Teams
      - Relations between Categories, Conferences, Teams
      - Site Languages
      - Social Networks support
      - Surveys
      - Banners
      - Advertisements

## Requirements

### Functional requirements

1. [Log in and sign up to the portal](/products/sport_news_portal/web_application_features/log_in_and_sign_up/)
2. [Page layout on the portal](/products/sport_news_portal/web_application_features/project_layout/)
3. [Site footer of the portal](/products/sport_news_portal/web_application_features/site_footer/)
4. [Maintain navigation on the portal](/products/sport_news_portal/web_application_features/maintain_navigation/)
5. [Manage teams on the portal](/products/sport_news_portal/web_application_features/manage_the_teams/)
6. [Social networks on the portal](/products/sport_news_portal/web_application_features/social_networks/)
7. [Site languages on the portal](/products/sport_news_portal/web_application_features/site_languages/)
8. [Manage articles on the portal](/products/sport_news_portal/web_application_features/manage_articles/)
9. [Articles - user side on the portal](/products/sport_news_portal/web_application_features/articles_user_side/)
10. [Home page of the portal](/products/sport_news_portal/web_application_features/home_page/)
11. [Lifestyle and Dealbook news](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/)
12. [Sports videos on the portal](/products/sport_news_portal/web_application_features/video_page/)
13. [The most popular and commented articles on the portal](/products/sport_news_portal/web_application_features/most_popular_and_commented/)
14. [Manage news partners on the portal](/products/sport_news_portal/web_application_features/manage_news_partners/)
15. [Comments block on the portal](/products/sport_news_portal/web_application_features/comments/)
16. [Global site search on the portal](/products/sport_news_portal/web_application_features/global_site_search/)
17. [Newsletter subscription](/products/sport_news_portal/web_application_features/newsletter_email/)
18. [Team hub: news about favorite teams](/products/sport_news_portal/web_application_features/team_hub/)
19. [User management on the portal](/products/sport_news_portal/web_application_features/user_management/)
20. [Banners on the portal](/products/sport_news_portal/web_application_features/banners/)
21. [Manage advertisements on the portal](/products/sport_news_portal/web_application_features/manage_ads/)
22. [Surveys on the portal](/products/sport_news_portal/web_application_features/surveys/)

### Non-functional requirements

- The application should use Cloud service for storing images and video files
- The application should be built following the REST principles
- The application must work in all modern browsers
- The application must be able to support 1000 simultaneous users

### Layout requirements

- The site inputs should have validation on the server side as well as on a client side (consider limiting input length, checking the input value format and type)
- The site links should be opened in a new tab
- The site links should be highlighted on hover
- The menu item that is currently active (meaning user is viewing it in the moment) should be highlighted

### User interface

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A2&viewport=592%2C442%2C1&scaling=min-zoom) to see a general clickable prototype.

## Audience

1. Sports fans.
2. People in search of the latest sports news.
3. People who want to receive sport news emails.

## Future work

1. Mobile support. Make sure that users can access the Sports Hub application using their mobile phone or tablet and the Sports Hub application layout is optimized.
2. Page templates list. Build support for admins to choose the page template when creating a new page for the Sports Hub application.
3. Admins with different sets of permissions. Build a possibility for admin users to define permissions for other admins in order to make it possible to create admins with limited access to CMS.
