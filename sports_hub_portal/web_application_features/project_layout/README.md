### Back to [Web site](../../#web-site) functional requirements

# Page layout on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

Create a Sports Hub site project layout structure that will be common for any of the pages:
  - Site header section
  - Site footer section
  - Site main navigation section on the left side
  - Main content area section
  - Right sidebar section

Also, there should be a special behavior of the site logo. It should navigate users to the home page. The external links (if any) should open in a new tab. Admin should have the ability to act as a regular user.
Please note, page content sections are configured by admin.

## Check list:

  - Verify if UI corresponds to the prototype
  - Users should go to the home page by clicking the logo
  - The layout structure should be the same for all pages
  - Third-party site should open in a separate browser tab when the user selects an external link
  - Pages should be built from content sections that are configured by admin
  - Admin should have the ability to act as a regular user and go back to the admin view

## Prototype of the feature

Please click [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A1586&viewport=-381%2C678%2C0.1179991066455841&scaling=min-zoom) and [here](https://www.figma.com/proto/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A2&viewport=454%2C441%2C0.038604091852903366&scaling=min-zoom) to see clickable prototypes.

Please click [here](https://www.figma.com/file/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A1) and [here](https://www.figma.com/file/JVDTph8VY9Ye7kz8BTDxhJ/1-Sport-News-General-Prototype?node-id=0%3A1073) to see mockups that were included in the prototypes and additional style guides.

Please click [here](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=54%3A6358&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to see style guides

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Page structure (user side): general sections**](/sports_hub_portal/web_application_features/project_layout/user_stories/user_side_general_page_structure)|<pre>As a site user<br>I want to view the same layout structure across all the pages</pre>
2 |[**Page structure (user side): user profile section in the header (user logged out)**](/sports_hub_portal/web_application_features/project_layout/user_stories/user_side_user_profile_section_logged_out_user)|<pre>As a site user<br>I want to see Sign up and Log in buttons when I am logged out</pre>
3 |[**Page structure (user side): user profile section in the header (user logged-in)**](/sports_hub_portal/web_application_features/project_layout/user_stories/user_side_user_profile_section_logged_in_user)|<pre>As a site user<br>I want to see my name when I am logged-in</pre>
4 |[**Page structure (user side): user profile pages (user logged-in)**](/sports_hub_portal/web_application_features/project_layout/user_stories/user_side_user_profile_empty_pages)|<pre>As a site user<br>I want to view personal profile pages when I am logged-in</pre>
5 |[**Page structure (admin side): general sections**](/sports_hub_portal/web_application_features/project_layout/user_stories/admin_side_general_page_structure)|<pre>As an admin user<br>I want to view the same layout structure across all the pages</pre>
6 |[**Page structure (admin side): header section**](/sports_hub_portal/web_application_features/project_layout/user_stories/admin_side_page_structure_header)|<pre>As an admin user<br>I want to view the header section</pre>
7 |[**Page structure (admin side): left vertical menu**](/sports_hub_portal/web_application_features/project_layout/user_stories/admin_side_left_vertical_menu)|<pre>As an admin user<br>I want to view the left vertical menu (local navigation)</pre>
8 |[**Page structure (admin side): user profile section in the header**](/sports_hub_portal/web_application_features/project_layout/user_stories/admin_side_user_profile_header_section)|<pre>As an admin user<br>I want to see my name when I am logged-in</pre>
9 |[**Page structure (admin side): switch to user view**](/sports_hub_portal/web_application_features/project_layout/user_stories/admin_side_switch_to_user_view)|<pre>As an admin user<br>I want to be able to swith to a user view</pre>
