# Manage Advertisements on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the Feature](#prototype-of-the-feature)
- [User Stories](#user-stories)

## Description

Logged in user should be able to see advertisement(s) at the top of the right sidebar on the site. Logged in user should be able to click on the advertisement and be redirected to the advertised website. The advertisement should be related to the category that they are viewing. 
The admin user should be able to configure the advertisements list (including adding new advertisement, closing active advertisement and disabling advertisement for the whole site). Two types of advertisements should be supported:
  - Category related
  - Site-wide 

When an admin user publishes a new advertisement, he can optionally choose the advertisement category. In case there is no category selected, then the advertisement is site-wide and can be shown at any page of the site. In case there is any category selected for the ad, then this ad should be displayed only at the site pages related to the specified category.

## Check list:

  - Verify if UI corresponds to prototype
  - Logged in user should be able to see advertisements at the right sidebar on the site
  - Logged in user should be able to click on the advertisement and be redirected to the advertised website
  - Admin user should be able to the advertisements list (including adding new advertisement, closing active advertisement and disabling advertisement for the whole site)
  - Category related and site-wide advertisements should be supported
  - Category related advertisements should be displayed only at the site pages related to the specified category
  - Site-wide advertisements should be shown at any page of the site

## Prototype of the feature

  Please click [here](https://www.figma.com/proto/egXgh8BYD7Xaa0JeMNhv9R/Manage-Ads?node-id=0%3A1075&scaling=min-zoom) to see a clickable prototype for the feature.

## User Stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure Advertisements**](/products/sport_news_portal/web_application_features/manage_ads/user_stories/configure_ads)|<pre>As an admin user<br>I want to be able to configure list of Advertisements<br>So that it is possible to promote products via the Sport News site</pre>
2 |[**Allow users to see Advertisements**](/products/sport_news_portal/web_application_features/manage_ads/user_stories/view_ads)|<pre>As a site user<br>I want to be able to view advertisement at the top of the right sidebar of the site</pre>
