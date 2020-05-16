# Manage News Partners on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the Feature](#prototype-of-the-feature)
- [User Stories](#user-stories)

## Description

User with admin permission should be able to manage integration with partners, namely:<br>
    - Configure a new partner<br>
    - View existing partners configurations<br>
    - Edit the existing partner's configurations<br>
    - Remove integration with the partner<br>
Integration can be configured only with a partner from the predefined list. 
Admin cannot add a new partner to the list. It is possible to add only one integration for one partner. 
The initial design is built for one partner - Google News (https://newsapi.org)

## Check list:

  - Admin should be able to configure a new partner
  - Admin should be able to view existing partners configurations
  - Admin should be able to edit the existing partner's configurations
  - Admin should be able to remove integration with the partner
  - Integration should be configured only with a partner from the predefined list
  - User should be able to view the list of existing partners configurations
  - All the buttons and pop-ups should not be corrupted
  - Web page content should be correct without any spelling or grammatical errors
  - All fonts should be the same as per the requirements

## Prototype of the feature

  Please click [here](https://www.figma.com/file/U7MdkpMsV1yimaWduSnzZP/News-Partners?node-id=4523%3A10122) to see a clickable prototype for the feature.

## User Stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure a new partner on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/configure_new_partner)|<pre>As an admin user<br>I want to be able to configure a new integration with partner<br>So that user will see the news from a third-party source</pre>
2 |[**Allow admin users to view an existing partner's configurations on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/viewing_existing_partners_configurations)|<pre>As an admin user<br>I want to be able to view the list of existing partners configurations</pre>
3 |[**Allow admin users to edit the existing partner's configurations on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/editing_existing_partners_configurations)|<pre>As an admin user<br>I want to be able to change the existing partner's configurations</pre>
3 |[**Allow admin users to delete the integration with the partner on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/deleting_integration_with_partner)|<pre>As an admin user<br>I want to be able to delete the existing integration with the partner</pre>
