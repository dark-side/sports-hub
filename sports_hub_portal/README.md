# Sports Hub portal

- [Problem](#problem)
- [Solution](#solution)
- [Goals and objectives](#goals-and-objectives)
- [User personas](#user-personas)
- [Requirements](#requirements)
  - [Functional requirements](#functional-requirements)
    - [Web site](#web-site)
    - [Mobile application](#mobile-application)
  - [Non-Functional requirements](#non-functional-requirements)
  - [Layout requirements](#layout-requirements)
- [User interface](#user-interface)
- [Audience](#audience)
- [Future work](#future-work)

## Problem

These days in the world filled with different kinds of news presented on various websites it’s rather hard and time consuming to find the information we need. When it comes to sports, fans spend a fair amount of time browsing the web in order to find hot news relevant to their best-loved kind of sports or their favorite league or team.

## Solution

Creating a sports news site and mobile application focused exclusively on the sports activities will allow users to effectively manage the news they want to see thus helping fans and people interested in sports to address the issue of information overdose on the web and save time when looking for the news consistent with their interests.

## Goals and objectives

Specific goals are:
1. To create a web-application allowing users:
  - to read news related to different kinds of sports
  - to subscribe to the sports news of their choice
  - to receive the newsletters via email
  - to manage the kind of news they want to see (e.g. news related to the specific kind of sports,league or team)

2. To create the Content Management System (CMS) allowing users with proper permission to define the structure and content of the web-application

3. To create a mobile application allowing users:
  - to read news related to different kinds of sports
  - to subscribe to the sports news of their choice
  - to receive the newsletters via email

## Audience

1. Sports fans.
2. People in search of the latest sports news.
3. People who want to receive sport news emails.

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
      - Sports Subcategories
      - Teams
      - Relations between Categories, Subcategories, Teams
      - Site Languages
      - Social Networks support
      - Surveys
      - Banners
      - Advertisements

**Unauthorized mobile application user (not logged in to the Sports Hub mobile application)**

    Available actions
      - View sports news (note: the structure of the news pages and the content of the pages (articles) are defined in the CMS)
      - Subscribe to receive sports news (note: there are a few different subscription types: General news, League news, Team news)
      - Share the news via the Social Media (when configured in the CMS)
      - Login/Sign up to the Sports Hub mobile application (including the Login/Sign up with the Social Networks if enabled in CMS)

**Authorised mobile application user (logged in to the Sports Hub mobile application)**

    Available actions:
      - Manage personal info
      - Manage team subscriptions
      - Manage surveys
      - Answer the surveys
      - Comment on an article
      - Actions available for an unauthorized user

## Requirements

### Functional requirements

#### Web site:

1. [Log in and sign up to the portal](/sports_hub_portal/web_application_features/log_in_and_sign_up/)
2. [Page layout on the portal](/sports_hub_portal/web_application_features/project_layout/)
3. [Site footer of the portal](/sports_hub_portal/web_application_features/site_footer/)
4. [Maintain navigation on the portal](/sports_hub_portal/web_application_features/maintain_navigation/)
5. [User personal cabinet](/sports_hub_portal/web_application_features/user_profile_update/)
6. [Social networks on the portal](/sports_hub_portal/web_application_features/social_networks/)
7. [Site languages on the portal](/sports_hub_portal/web_application_features/site_languages/)
8. [Manage articles on the portal](/sports_hub_portal/web_application_features/manage_articles/)
9. [Articles - user side on the portal](/sports_hub_portal/web_application_features/articles_user_side/)
10. [Home page of the portal](/sports_hub_portal/web_application_features/home_page/)
11. [Lifestyle and Dealbook news](/sports_hub_portal/web_application_features/lifestyle_dealbook_news/)
12. [Sports videos on the portal](/sports_hub_portal/web_application_features/video_page/)
13. [The most popular and commented articles on the portal](/sports_hub_portal/web_application_features/most_popular_and_commented/)
14. [Manage news partners on the portal](/sports_hub_portal/web_application_features/manage_news_partners/)
15. [Comments block on the portal](/sports_hub_portal/web_application_features/comments/)
16. [Global site search on the portal](/sports_hub_portal/web_application_features/global_site_search/)
17. [Newsletter subscription](/sports_hub_portal/web_application_features/newsletter_email/)
18. [Team hub: news about favorite teams](/sports_hub_portal/web_application_features/team_hub/)
19. [User management on the portal](/sports_hub_portal/web_application_features/user_management/)
20. [Banners on the portal](/sports_hub_portal/web_application_features/banners/)
21. [Manage advertisements on the portal](/sports_hub_portal/web_application_features/manage_ads/)
22. [Surveys on the portal](/sports_hub_portal/web_application_features/surveys/)

#### Mobile application:

1. [Log in and sign up in the application](/sports_hub_portal/mobile_application_features/log_in_and_sign_up/)
2. [Page layout](/sports_hub_portal/mobile_application_features/project_layout/)
3. [Application footer](/sports_hub_portal/mobile_application_features/application_footer/)
4. [Navigation in the application](/sports_hub_portal/mobile_application_features/navigation/)
5. [Follow us on social networks](/sports_hub_portal/mobile_application_features/follow_on_social_networks/)
6. [Application languages](/sports_hub_portal/mobile_application_features/application_languages/)
7. [View articles in the application](/sports_hub_portal/mobile_application_features/articles_view/)
8. [Home page in the application](/sports_hub_portal/mobile_application_features/home_page/)
9. [Lifestyle and Dealbook news](/sports_hub_portal/mobile_application_features/lifestyle_dealbook_news/)
10. [Sports videos](/sports_hub_portal/mobile_application_features/video_page/)
11. [The most popular and commented articles](/sports_hub_portal/mobile_application_features/most_popular_and_commented/)
12. [News from Sports Hub partners](/sports_hub_portal/mobile_application_features/news_partners/)
13. [Comments block](/sports_hub_portal/mobile_application_features/comments/)
14. [Global application search](/sports_hub_portal/mobile_application_features/global_application_search/)
15. [Newsletter subscription](/sports_hub_portal/mobile_application_features/newsletter_email/)
16. [Team hub: news about favorite teams](/sports_hub_portal/mobile_application_features/team_hub/)
17. [Banners in the application](/sports_hub_portal/mobile_application_features/banners/)
18. [Advertisements](/sports_hub_portal/mobile_application_features/advertisements/)
19. [Surveys](/sports_hub_portal/mobile_application_features/surveys/)

### Non-functional requirements

- The application should use Cloud service for storing images and video files
- The application should be built following the REST principles
- The application must work in all modern browsers
- The application must be able to support 1000 simultaneous users

### Layout requirements

Please follow (the style guides)[https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368] of this product for each feature.

- The site inputs should have validation on the server side as well as on a client side (consider limiting input length, checking the input value format and type)
- The site links should be opened in a new tab
- The site links should be highlighted on hover
- The menu item that is currently active (meaning user is viewing it in the moment) should be highlighted

### User interface

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A2&viewport=592%2C442%2C1&scaling=min-zoom) to see a general clickable prototype.

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sports-Hub-General-Prototype?page-id=0%3A5852&node-id=0%3A5853&viewport=284%2C263%2C0.04008595272898674&scaling=scale-down) to see a mobile application clickable prototype.

## Future work

1. Page templates list. Build support for admins to choose the page template when creating a new page for the Sports Hub application.
2. Admins with different sets of permissions. Build a possibility for admin users to define permissions for other admins in order to make it possible to create admins with limited access to CMS.
