### Back to [Web site](../../#web-site) functional requirements

# Maintain navigation on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

A navigation menu should be visible on every page of the Sports Hub site on the left side. The navigation menu consists of the following menu items:
  - Home
  - News pages configured by admin (e.g. NFL, NBA, Golf, Soccer, etc.)
  - Lifestyle
  - Dealbook
  - Video
  - Team hub

The Home, Lifestyle, Dealbook, Video, and Team hub menu items are static categories.
Site admins can add as many sports categories as they prefer. If there are lots of the sports categories configured, then there should be a scroll bar added to the menu section.

Some of the sports categories have subcategories. Subcategories contain a list of the teams related to them. For example, the NFL sports category consists of the following subcategories: AFC East, AFC North, AFC South. The AFC South contains the following teams: Houston, Indianapolis, Jacksonville, Tennessee.

When users hover over a category in the main navigation menu that consists of the subcategories, this category is highlighted and a drop-down menu with links to the subcategories appears on the UI. When users select the subcategory, they are redirected to the subcategory news page.
When users hover over the subcategory in the secondary navigation menu that consists of the teams, this subcategory is highlighted and a drop-down menu with the list of teams appears on the UI. When users select the team, they are redirected to a team news page.

The Lifestyle, Dealbook, Video, and Team hub menu categories do not have subcategories, so when users hover over one of these categories, only this category is highlighted. When users select one of these categories, they are redirected to the appropriate category news page.
Admin user configures a list of categories, subcategories, and teams visible in the navigation menu.

The user with admin permissions should be able to manage teams, namely:
  - Add a new team
  - View existing teams
  - Edit an existing team
  - Remove an existing team
  - Filter existing teams

## Check list:

  - Verify if UI corresponds to the prototype
  - The navigation menu should be present on every page of the Sports Hub site
  - Admin user should be able to configure the navigation menu categories, subcategories, and teams
  - Admin should be able to add a new team using selectors
  - Admin should be able to add a new team using the map
  - Admin should be able to view information about already added teams
  - Admin should be able to edit existing teams
  - Admin should be able to remove existing teams
  - Admin user should be able to filter existing teams
  - Users should be able to go to the sports subcategory page of the Sports Hub site by using the navigation menu
  - Users should be able to navigate to the team page of the Sports Hub site by using the navigation menu

## Prototype of the feature

_Admin side_

Please click [here](https://www.figma.com/proto/MejavVSuDAMfSDu27O108g/Maintain-Navigation?node-id=0%3A1075&viewport=-177%2C284%2C0.04348461702466011&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/MejavVSuDAMfSDu27O108g/Maintain-Navigation?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

Please click [here](https://www.figma.com/proto/HB6RaAViOl1Iw5qCsEb2gj/Manage-teams?node-id=0%3A1075&viewport=-627%2C353%2C0.028726190328598022&scaling=scale-down) to see a clickable prototype.

Please click [here](https://www.figma.com/file/HB6RaAViOl1Iw5qCsEb2gj/Manage-teams?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

_User side_

Please click [here](https://www.figma.com/proto/MejavVSuDAMfSDu27O108g/Maintain-Navigation?node-id=0%3A2&viewport=210%2C442%2C0.08585662394762039&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/MejavVSuDAMfSDu27O108g/Maintain-Navigation?node-id=0%3A1) to see mockups that were included in the prototype and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to create navigation menu items on the portal**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/manage_navigation_items)|<pre>As an admin user<br>I want to create the navigation menu categories, subcategories, and teams visible to the site users</pre>
2 |[**Allow admin user to show and hide navigation menu items on the portal**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/hide_show_navigation_items)|<pre>As an admin user<br>I want to show and hide the navigation menu categories, subcategories, and teams on the portal</pre>
3 |[**Allow admin user to change order of the navigation menu items and move them between the categories and subcategories**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/move_and_order_navigation_items)|<pre>As an admin user<br>I want to change order of the navigation menu items and move them between the categories and subcategories</pre>
4 |[**Allow admin users to add a new team on the portal**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/add_new_team)|<pre>As an admin user<br>I want to add a new team</pre>
5 |[**Allow admin users to edit the existing team**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/edit_existing_team)|<pre>As an admin user<br>I want to edit the existing team</pre>
6 |[**Allow admin users to filter and search the teams**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/filter_teams)|<pre>As an admin user<br>I want to filter the Teams page</pre>
7 |[**Allow admin users to delete the existing team**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/delete_team)|<pre>As an admin user<br>I want to delete the existing team</pre>
8 |[**Allow site users to navigate to the sports categories, subcategories, and teams page on the portal**](/sports_hub_portal/web_application_features/maintain_navigation/user_stories/navigation_user_side)|<pre>As a site user<br>I want to view the navigation menu on every page of the Sports Hub site<br>So that I can navigate between sports categories, subcategories, and teams news pages</pre>
