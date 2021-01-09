# Banners on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

Site users should be able to see banners on the right sidebar to see reminders about upcoming events, etc. The banner(s) should be related to the category that they are viewing. 
For example, if a user views a page from the NBA category, then banner(s) related to the NBA category should be displayed in the right sidebar.
Also, there should be predefined banners for Facebook Video, Facebook Post, Lifestyle, Dealbook. The admin user should be able to show/hide the predefined banners.
The admin user should configure the banners visible per category as well as the banner content. The banners will be rotating every 3 seconds in case of more than one banner in the category.

## Check list:

  - Verify if UI corresponds to prototype
  - The right sidebar should be visible for site users
  - The banners should be related to the category, for example, the banner(s) related to the NBA category only should be displayed at the right sidebar
  - There should be predefined banners visible for site users
  - Admin user should be able to configure the banners visible per category
  - Admin user should be able to configure the banner content
  - In case of more than one banner in the category banners will be rotating each 3 seconds
  - Admin user should be able to publish banners
  - Admin user should be able to delete closed banners
  - Admin user should be able to show predefined banners (Facebook Video, Facebook Post, Lifestyle, Dealbook)
  - Admin user should be able to hide predefined banners (Facebook Video, Facebook Post, Lifestyle, Dealbook)

## Prototype of the feature

Please click [here](https://www.figma.com/proto/RbCgwAjOZqzLJhyEpxG5Ez/Banners?node-id=0%3A2335&viewport=-3340%2C642%2C0.12847007811069489&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/RbCgwAjOZqzLJhyEpxG5Ez/Banners?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin users to configure banners on the portal**](/products/sport_news_portal/web_application_features/banners/user_stories/configure_banners)|<pre>As an admin user<br>I want to configure a list of banners<br>So that users can see them while viewing the Sport News site</pre>
2 |[**Allow users to view configured banners on the portal**](/products/sport_news_portal/web_application_features/banners/user_stories/view_banner)|<pre>As a site user<br>I want to view banners in the right sidebar of the site<br>So that I can see reminders about upcoming sport events, important updates, etc</pre>
3 |[**Allow admin users to configure predefined banners on the portal**](/products/sport_news_portal/web_application_features/banners/user_stories/configure_predefined_banners)|<pre>As an admin user<br>I want to configure predefined banners on the portal</pre>
4 |[**Allow site users to view predefined Lifestyle and Dealbook banners on the portal**](/products/sport_news_portal/web_application_features/banners/user_stories/view_pedefined_lifestyle_dealbook_banners)|<pre>As a site user<br>I want to view predefined Lifestyle and Dealbook banners on the portal</pre>
5 |[**Allow site users to view predefined Facebook banners on the portal**](/products/sport_news_portal/web_application_features/banners/user_stories/view_pedefined_facebook_banners)|<pre>As a site user<br>I want to view predefined Facebook banners on the portal</pre>
