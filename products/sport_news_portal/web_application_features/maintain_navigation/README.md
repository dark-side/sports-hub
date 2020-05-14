# Maintain Navigation on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the Feature](#prototype-of-the-feature)
- [User Stories](#user-stories)

## Description

There should be a Navigation menu visible on every page of the Sport News site in the left side of every page. The Navigation menu consists of the following menu items:<br>
    - HOME<br>
    - NFL<br>
    - NBA<br>
    - MLB<br>
    - NHL<br>
    - CBB<br>
    - CFB<br>
    - NASCAR<br>
    - GOLF<br>
    - SOCCER<br>
    - LIFESTYLE<br>
    - DEALBOOK<br>
    - VIDEO<br>
    - TEAM HUB<br>
    - Follow on social block (Facebook, Twitter, Google +, Youtube)<br>
The HOME, LIFESTYLE, DEALBOOK, VIDEO and TEAM HUB menu items are static categories. The NFL, NBA, MLB, NHL, CBB, CFB, NASCAR, GOLF and SOCCER are sport categories configurable by Admin. Site admin can add as many sport categories as he prefers. If there are more than eight sport categories configured than there should be a scroll added to the menu section.   
Some of the sport categories are divided into subcategories. The subcategories contain a list of the teams related to the subcategory. 
For example the NFL sport category consists of the following subcategories: AFC East, AFC North, AFC South, AFC West, NFC East, NFC North, NFC South, NFC West. The AFC South contains the following teams: Houston, Indianapolis, Jacksonville, Tennessee
When a logged in user hovers over the category in the main navigation menu that consists of the subcategories, then this category is highlighted and a mega dropdown menu with links to the subcategories appear in the UI. When a logged in user clicks on the subcategory, he is redirected to the subcategory page
When a logged in user hovers over the subcategory in the secondary navigation menu that consists of the teams, then this subcategory is highlighted and a dropdown menu with list of teams appears in the UI. When a logged in user clicks on the team, he is redirected to the team page
The LIFESTYLE, DEALBOOK, VIDEO and TEAM HUB Navigation menu categories don’t have subcategories, so when a logged in user hovers over one of these categories, then this category is only highlighted. When a logged in user clicks on one of these categories, he is redirected to the appropriate category page
Admin user configures a list of categories, subcategories and teams visible in the Navigation panel

## Check list:

  - Verify if UI corresponds to prototype
  - Navigation should be present on every page of the Sport News site
  - Admin user should be able to configure the Navigation menu categories, subcategories and teams
  - Logged in user should be able to navigate to the sport subcategory page of the Sport News site using the Navigation menu
  - Logged in user should be able to navigate to the team page of the Sport News site using the Navigation menu
  - Page content should be valid without any spelling or grammatical errors
  - All fonts should be same as per the requirements

## Prototype of the feature

  Please click [here](https://www.figma.com/file/MejavVSuDAMfSDu27O108g/Maintain-Navigation?node-id=4523%3A10122) to see a clickable prototype for the feature.

## User Stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin users to manage navigation items on the portal**](/products/sport_news_portal/web_application_features/maintain_navigation/user_stories/manage_navigation_items)|<pre>As an admin user<br>I want to be able to configure the Navigation menu categories, subcategories and teams<br>So that I have control over the sport categories, subcategories and teams visible to the site users</pre>
2 |[**Allow users to view the navigation menu on the portal**](/products/sport_news_portal/web_application_features/maintain_navigation/user_stories/main_navigation)|<pre>As a site user<br>I want to be able to views the Navigation menu on every page of the Sport News site<br>So that I can navigate between sport categories pages</pre>
3 |[**Allow users to navigate to the sport subcategory page on the portal**](/products/sport_news_portal/web_application_features/maintain_navigation/user_stories/main_navigation_dropdowns)|<pre>As a site user<br>I want to be able to navigate to the sport subcategory page of the Sport News site using the Navigation menu<br>So that I can see news about selected subcategory</pre>
4 |[**Allow users to navigate to the team page on the portal**](/products/sport_news_portal/web_application_features/maintain_navigation/user_stories/secondary_navigation)|<pre>As a site user<br>I want to be able to navigate to the team page of the Sport News site using the Navigation menu<br>So that I can see news about selected team</pre>
