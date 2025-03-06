### Back to [Mobile application](/mobile_application_features/mobile_application_features_list/README.md) functional requirements

# Navigation in the application

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

A navigation menu should be visible on every page of the Sports Hub application expandable on the left side of every page. The main navigation menu consists of the following menu items:
  - Home
  - Category1
  - Category2
  - ...
  - CategoryN
  - Team hub
  - Lifestyle
  - Dealbook
  - Video
  - Language icons

The Home, Team hub, Lifestyle, Dealbook and Video menu items are static categories. The Category1, Category2, ..., CategoryN are sports categories configurable by admin.

Some of the sports categories have subcategories. The subcategories contain a list of teams related to the subcategory.

When users tap a category in the main navigation menu that consists of the subcategories, this category is selected and a list with links to the subcategories appears on the UI. When users tap the subcategory, they are redirected to the subcategory page.

When users tap the subcategory arrow icon, this subcategory is expanded with a list of teams. When users tap the team, they are redirected to a team page.

The Lifestyle, Dealbook, Video, and Team hub menu categories don’t have subcategories, so when users tap one of these categories, they are redirected to the appropriate category page.

## Check list:

  - Verify if UI corresponds to the prototype
  - Navigation menu should be present on every page of the Sports Hub application
  - Users should be able to go to the sports subcategory page of the Sports Hub application by using the navigation menu
  - Users should be able to navigate to the team page of the Sports Hub application by using the navigation menu

## Prototype of the feature

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sports-Hub-General-Prototype?page-id=0%3A5852&node-id=0%3A7481&viewport=-1637%2C-969%2C0.37520089745521545&scaling=scale-down) to see a clickable prototype.

Please click [here](https://www.figma.com/design/JVDTph8VY9Ye7kz8BTDxhJ/%231---Sports-Hub-General-Prototype?node-id=0-5852&t=QqYNpKrPFqpmBfIT-1) to see mockups that were included in the prototype and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow users to navigate to the sports categories, subcategories, and teams page in the application**](/mobile_application_features/navigation/user_stories/navigation_user_side/README.md)|<pre>As a user<br>I want to view the navigation menu on every page of the Sports Hub application<br>So that I can navigate between sports categories, subcategories, and teams news pages</pre>
