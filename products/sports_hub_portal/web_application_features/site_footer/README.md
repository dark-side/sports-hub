# Site footer of the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

The footer section should be visible on every page of the Sports Hub site.
All footer sections should be configurable by the admin user. The admin defines which section to show in the footer as well as the content of each section.

The footer section should contain three columns: Company info, Contributors, Newsletter, Sports Hub logo, the copyright sign, and the <b>Privacy</b> and <b>Terms</b> links at the bottom of the page.

The Company info column should consist of the following links:
  - About Sports Hub
  - News / In the Press
  - Advertising / Sports Blogger Ad Network
  - Events
  - Contact Us

The Contributors column should consist of the following links:
  - Featured Writers Program
  - Featured Team Writers Program
  - Internship Program

The admin should be able to change the <b>Privacy policy</b> and <b>Terms and conditions</b> link names, and content but should not hide or delete them.

The Newsletter is described [in separate feature](/products/sports_hub_portal/web_application_features/newsletter_email)

## Check list:

  - Verify if UI corresponds to the prototype
  - Admin user should be able to configure the columns of the site footer
  - Admin user should be able to configure the content of the columns of the site footer
  - Admin user should be able to edit the content of the links of the site footer for <b>Company info</b> and <b>Contributors</b> tabs
  - Admin user should be able to add new footer items for <b>Company info</b> and <b>Contributors</b> tabs
  - Admin user cannot delete the <b>About Sports Hub</b> or <b>Contact Us</b> items on the <b>Company info</b> tab
  - Admin user cannot delete the <b>Sign up to receive the latest sports news</b> item on the <b>Newsletter</b> tab
  - Admin user should be able to configure the names and content of the <b>Privacy policy</b> and <b>Terms and conditions</b> links
  - Admin user shouldn’t be able to hide or delete the <b>Privacy policy</b> and <b>Terms and conditions</b> links
  - Admin user shouldn’t be able to add new items for the <b>Privacy and Terms</b> tab
  - Users should be able to see the site footer on every page of the Sports Hub site
  - Users should be able to see the links to the pages to read more about the company, contributors and subscribe to receive the latest news
  - Users should be able to subscribe to the Sports Hub site
  - Users should be able to see the <b>Privacy policy</b> and <b>Terms and conditions</b> links
  - All the links should be clickable and work properly

## Prototype of the feature

_Admin side_

Please click [here](https://www.figma.com/proto/7AUcQB82LimoDlaD7rl4uw/Site-Footer?node-id=0%3A2345&viewport=-3358%2C515%2C0.10175449401140213&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/7AUcQB82LimoDlaD7rl4uw/Site-Footer?node-id=0%3A3859) to see mockups that were included in the prototype and additional style guides.

_User side_

Please click [here](https://www.figma.com/proto/7AUcQB82LimoDlaD7rl4uw/Site-Footer?node-id=0%3A2&viewport=502%2C286%2C0.10842359811067581&scaling=min-zoom) to see a clickable prototype.

Please click [here](https://www.figma.com/file/7AUcQB82LimoDlaD7rl4uw/Site-Footer?node-id=0%3A1) to see mockups that were included in the prototype and additional style guides.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure site footer**](/products/sports_hub_portal/web_application_features/site_footer/user_stories/configure_site_footer)|<pre>As an admin user<br>I want to be able to configure site footer sections, links, and content</pre>
2 |[**Allow users view site footer on the portal**](/products/sports_hub_portal/web_application_features/site_footer/user_stories/view_site_footer)|<pre>As a site user<br>I want to be able to see a site footer on every page of the Sports Hub site with the links configured by admin</pre>
