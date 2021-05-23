# Home page of the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

When users visit our site, they should see the main page by default. The main page is called <b>Home</b> in the navigation menu. This page should contain the most recent news and topics, and consist of the following page sections:
  - <b>Main articles</b>: Admin can add at least 1 and up to 5 articles to the section. These articles will be rotating every 3 seconds. This section needs to be always present and users can not hide it on the page. Users can select the article number to make a rotation to it. Rotation will continue from the selected article. The section is always present and can not be hidden.
  - <b>Breakdown</b>: Admin can show or hide this section on the page. The <b>Breakdown</b> section has to consist of breakdowns with 2-4 articles.

Admin user can show and hide the following sections:
  - <b>Photo of the day</b>
  - <b>Most popular</b>
  - <b>Most commented</b>

We want to allow the admin user to configure this page, post articles, photos, and make some parts of the page visible or hidden.
The <b>Most popular</b> and <b>Most commented</b> functionalities are described in [the separate feature](/products/sports_hub_portal/web_application_features/home_page/user_stories/most_popular_and_commented).

## Check list:

  - Verify if UI corresponds to the prototype
  - Users should be able to see the <b>Main articles</b> section on the <b>Home</b> page
  - Users should be able to view the <b>Photo of the day</b> section on the <b>Home</b> page
  - Users should be able to see the <b>Breakdown</b> section on the <b>Home</b> page
  - Users should be able to navigate to another page of the site on the <b>Home</b> page
  - Admin user shouldn’t be able to hide the <b>Main articles</b> section from users
  - Admin user should be able to set up the <b>Breakdown</b> section for a specific category
  - Admin user should be able to show the <b>Breakdown</b> section and hide it from users
  - Admin user should be able to configure the <b>Photo of the day</b> section for users
  - Admin user should be able to show the <b>Photo of the day</b> section and hide it from users

## Prototype of the feature

_Admin side_

Please click [here](https://www.figma.com/proto/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=0%3A1074&viewport=-716%2C546%2C0.10301588475704193&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

_User side_

Please click [here](https://www.figma.com/proto/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=0%3A2&viewport=530%2C561%2C0.07127833366394043&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/BpGy9tY0mE6hfw0hUN2Qeb/Home-Page?node-id=0%3A1) to see mockups that were included in the prototype and additional style guides.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure the Main articles section**](/products/sports_hub_portal/web_application_features/home_page/user_stories/configuration_of_main_articles_block)|<pre>As an admin user<br>I want to set up up to 5 main articles<br>So that site users can see them on the <b>Home</b> page</pre>
2 |[**Display the Main articles section for site users on the Home page**](/products/sports_hub_portal/web_application_features/home_page/user_stories/display_main_articles_for_user)|<pre>As a site user<br>I want to see the Main articles section on the <b>Home</b> page</pre>
3 |[**Allow admin user to configure the Breakdown section**](/products/sports_hub_portal/web_application_features/home_page/user_stories/configuration_of_breakdown_block)|<pre>As an admin user<br>I want to set up the <b>Breakdown</b> section news for a specific category<br>So that site users can see them on the <b>Home</b> page</pre>
4 |[**Display the Breakdown section for site users on the Home page**](/products/sports_hub_portal/web_application_features/home_page/user_stories/display_breakdown_for_user)|<pre>As a site user<br>I want to see the <b>Breakdown</b> section on the <b>Home</b> page</pre>
5 |[**Allow admin user to configure the Photo of the day section**](/products/sports_hub_portal/web_application_features/home_page/user_stories/configuration_of_photo_of_the_day_block)|<pre>As an admin user<br>I want to be able to set up <b>Photo of the day</b><br>So that site users can see it on the <b>Home</b> page</pre>
6 |[**Display Photo of the day for site users on the Home page**](/products/sports_hub_portal/web_application_features/home_page/user_stories/display_photo_of_the_day_for_user)|<pre>As a site user<br>I want to see <b>Photo of the day</b> on the <b>Home</b> page</pre>
7 |[**Allow admin user to preview the Home page**](/products/sports_hub_portal/web_application_features/home_page/user_stories/home_page_preview)|<pre>As an admin user<br>I want to be able to preview the <b>Home</b> page while configuration<br>So that I could review the page as a site user</pre>
