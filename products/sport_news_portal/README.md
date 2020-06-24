# Sport News Portal

- [Problem](#problem)
- [Solution](#solution)
- [Goals and Objectives](#goals-and-objectives)
- [User Personas](#user-personas)
- [Requirements](#requirements)
  - [Functional Requirements](#functional-requirements)
  - [Non-Functional Requirements](#non-functional-requirements)
  - [Layout Requirements](#layout-requirements)
- [User Interface](#user-interface)
- [Audience](#audience)
- [Future Work](#future-work)

## Problem

Nowadays the world is filled in with different kinds of news and news sites, but often it’s hard and time consuming to find the news you are interested in. When it comes to sports, sport fans need to spend a fair amount of time browsing through the web in order to find the sport news relevant to their favorite kind of sport or their favorite league or team.

## Solution

Creating a sport news site that is focused only on the news about different sport activities and allows users to effectively manage the news that they want to see will help sport fans and people who are interested in sport to solve the problem with the information overdose in the web and save their time when looking for the news relevant to their interest.

## Goals and Objectives

Specific goals are:
1. Create a web-application that allows users the following:
  - to read sport news related to different kinds of sport
  - to subscribe to receive the news about their favorite kind of sport or league or team 
  - to receive the newsletter emails
  - to manage the kind of news they want to see (eg.: news related to specific kind of sport or league or team) what kind of news
2. Create a Content Management System that allows users with proper permissions to define the structure and content of the web-application

## User Personas

**Not authorised website user (not logged in to the Sport News site)**

    Available actions
      - View sport news (note: the structure of the news pages and the content of the pages (articles) are defined in the CMS)
      - Subscribe to receive sport news (note: there are few different subscription types - General news, League news, Team news)
      - Share the news via the Social Media (when configured in the CMS)
      -Login/Sign up to the Sport News site (including the Login/Sign up with the Social Networks if enabled in CMS)

**Authorised website user (logged in to the Sport News site)**

    Available actions:
      - Manage personal info
      - Manage team subscriptions
      - Manage surveys
      - Answer the surveys
      - Comment an article
      - Actions available for not authorized user

**Website Admin**

    Available actions:
    Can configure the following parts of the site via the CMS:
      - Site footer
      - Site menu (including nested menu dropdowns)
      - Site users
      - Structure of the pages
      - Articles
      - Sport Categories (Leagues)
      - Sport Conferences
      - Teams
      - Relations between Categories, Conferences, Teams
      - Site Languages
      - Social Networks support
      - Surveys
      - Banners
      - Advertises

## Requirements

### Functional Requirements

1. [Log In and Sign Up to the portal](/products/sport_news_portal/web_application_features/log_in_and_sign_up/)
2. [Page Layout on the portal](/products/sport_news_portal/web_application_features/project_layout/)
3. [Global site search on the portal](/products/sport_news_portal/web_application_features/global_site_search/)
4. [Site Footer of the portal](/products/sport_news_portal/web_application_features/site_footer/)
5. [Site Languages on the portal](/products/sport_news_portal/web_application_features/site_languages/)
6. [Home page of the portal](/products/sport_news_portal/web_application_features/home_page/)
7. [Most Popular/Commentable articles on the portal](/products/sport_news_portal/web_application_features/most_popular_and_commentable/)
8. [Social Networks on the portal](/products/sport_news_portal/web_application_features/social_networks/)
9. [Surveys on the portal](/products/sport_news_portal/web_application_features/surveys/)
10. [Manage Articles of the portal](/products/sport_news_portal/web_application_features/manage_articles/)
11. [Articles User Side on the portal](/products/sport_news_portal/web_application_features/articles_user_side/)
12. [Banners on the portal](/products/sport_news_portal/web_application_features/banners/)
13. [Maintain Navigation on the portal](/products/sport_news_portal/web_application_features/maintain_navigation/)
14. [Video Page of the portal](/products/sport_news_portal/web_application_features/video_page/)
15. [League and Team Page of the portal](/products/sport_news_portal/web_application_features/league_and_team_page/)
16. [Dealbook Page of the portal](/products/sport_news_portal/web_application_features/dealbook_page/)
17. [Manage teams on the portal](/products/sport_news_portal/web_application_features/manage_the_teams/)
18. [Manage Advertisements on the portal](/products/sport_news_portal/web_application_features/manage_ads/)
19. [Manage Pages on the portal](/products/sport_news_portal/web_application_features/manage_pages/)
20. [Lifestyle – Sidebar Block](/products/sport_news_portal/web_application_features/lifestyle_sidebar_block/)
21. [User Management on the portal](/products/sport_news_portal/web_application_features/user_management/)
22. [Newsletter Email](/products/sport_news_portal/web_application_features/newsletter_email/)
23. [Manage News Partners on the portal](/products/sport_news_portal/web_application_features/manage_news_partners/)
24. [Comments block on the portal](/products/sport_news_portal/web_application_features/comments/)

### Non-Functional Requirements

- The application should use Cloud service for storing images and video files.
- The application should be built following the REST principles.
- The application must work in all modern browsers.
- The application must be able to support 1000 simultaneous users.

### Layout Requirements

- The site inputs should have validation on the server side as well as on a client side (consider limiting input length, checking the input value format and type).
- The site links should be opened in a new tab.
- The site links should be highlighted on hover.
- The menu item that is currently active (meaning user is viewing it in the moment) should be highlighted.

### User Interface

Please click [here](https://www.figma.com/file/JVDTph8VY9Ye7kz8BTDxhJ/%231---Sport-News-General-Prototype) to see the mockups.

## Audience

1. Sport fans.
2. People who want to get latest sport news.
3. People who want to receive sport news emails.

## Future Work

1. Mobile support. Make sure that users can access the Sport news application using their mobile phone or tablet and the the Sport news application layout is optimized for use by mobile phone or tablet.
2. Page templates list. Build support for admin to choose the page template when they create a new page for a Sport news application.
3. Admins with different sets of permissions. Build possibility for admin users to define permissions for other admins in order to make it possible to create admins with limited access to CMS.
