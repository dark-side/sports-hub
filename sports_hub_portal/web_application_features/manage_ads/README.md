### Back to [Web site](../../#web-site) functional requirements

# Manage advertisements on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

Users should be able to see advertisements at the top of the right sidebar of the site. Users should be able to click on the advertisement and then be redirected to the advertised website. The advertisement should be related to the category that is being viewed.
The admin user should be able to configure the advertisements list: add new advertisements, edit, delete, and disable advertisements for the whole site. Two types of advertisements should be supported:
  - Category related
  - Site-wide

When an admin user publishes a new advertisement, they can optionally choose the advertisement category. If no category is selected, the advertisement is site-wide and will be shown on any page of the site. If a category is selected for an ad, this ad should be displayed only on the site pages related to the selected category.
When there is more than one ad that should be shown in the category, ads will be rotating every 3 seconds.

## Check list:

  - Verify if UI corresponds to the prototype
  - Users should be able to see advertisements at the right sidebar of the site
  - Users should be able to click on the advertisement and be redirected to the advertised website
  - Admin user should be able to edit the advertisements list (including adding new advertisements, editing advertisements, deleting advertisements, and disabling advertisements for the whole site)
  - Category related and site-wide advertisements should be supported
  - Category related advertisements should be displayed only on the site pages related to the specified category
  - Site-wide advertisements should be shown on any page of the site
  - Advertisements will be rotating every 3 seconds in case more than one ad is displayed

## Prototype of the feature

Please click [here](https://www.figma.com/proto/egXgh8BYD7Xaa0JeMNhv9R/Manage-Ads?node-id=0%3A1075&viewport=-2341%2C634%2C0.1026575043797493&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/egXgh8BYD7Xaa0JeMNhv9R/Manage-Ads?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure advertisements**](/sports_hub_portal/web_application_features/manage_ads/user_stories/configure_ads)|<pre>As an admin user<br>I want to configure the list of advertisements<br>So that it is possible to promote them via the Sports Hub site</pre>
2 |[**Allow users to see advertisements**](/sports_hub_portal/web_application_features/manage_ads/user_stories/view_ads)|<pre>As a site user<br>I want to view an advertisement on the top of the right sidebar of the site</pre>
