# Manage News Partners on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [User stories](#user-stories)

## Description

User with admin permission should be able to manage integration with partners, namely:
  - Сonfigure a new partner
  - View existing partners configurations
  - Edit the existing partner's configurations
  - Remove integration with the partner
Integration can be configured only with a partner from the predefined list. Admin cannot add a new partner to the list. It is possible to add only one integration for one partner. The initial design is built for one partner - Google News (https://newsapi.org).
News from the configured partner should be shown directly to the users and shouldn’t be available among news to edit them by admin.

## Check list:

  - Verify if UI corresponds to prototype
  - Admin should be able to configure a new partner
  - Admin should be able to view existing partners configurations
  - Admin should be able to edit the existing partner's configurations
  - Admin should be able to remove integration with the partner
  - Integration should be configured only with a partner from the predefined list
  - News from configured partner shouldn’t be available in the news list for admin to configure them as articles
  - User should be able to view the news from the partner configured

## Prototype of the feature

  Please click [here](https://www.figma.com/file/U7MdkpMsV1yimaWduSnzZP/News-Partners?node-id=4523%3A10122) to see a clickable prototype for the feature.

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure a new partner on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/configure_new_partner)|<pre>As an admin user<br>I want to be able to configure a new integration with a partner<br>So that user will see the news from a third-party source</pre>
2 |[**Allow admin user to activate/deactivate news partners**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/activate_deactivate_partner)|<pre>As an admin user<br>I want to be able to activate or deactivate existing partners</pre>
3 |[**Allow admin user to edit the existing partner's configurations on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/editing_existing_partners_configurations)|<pre>As an admin user<br>I want to be able to change the existing partner's configurations</pre>
4 |[**Allow admin user to delete the integration with the partner on the portal**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/deleting_integration_with_partner)|<pre>As an admin user<br>I want to be able to delete the existing integration with the partner</pre>
5 |[**Allow site user to view news from the configured partners**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/viewing_news_from_partners)|<pre>As a site user<br>I want to be able to see the news from the configured partners in the appropriate categories</pre>
6 |[**News from the configured partners can not be edited by the admin**](/products/sport_news_portal/web_application_features/manage_news_partners/user_stories/partners_news_admin_editability)|<pre>As an admin user<br>I should not to see the news from the configured partners in the articles list page</pre>
