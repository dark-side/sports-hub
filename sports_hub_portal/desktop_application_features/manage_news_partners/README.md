### Back to [Desktop application](../../#desktop-application) functional requirements

# Manage news partners on the portal

- [Description](#description)
- [Check list](#check-list)
- [Prototype of the feature](#prototype-of-the-feature)
- [Style guides](#style-guides)
- [User stories](#user-stories)

## Description

Users with admin permission should be able to manage integration with partners, namely:
  - Сonfigure new partners
  - View the existing partners’ configurations
  - Edit the existing partners’ configurations
  - Remove integration with partners

Integration can be configured only with partners from the predefined list.
Admin cannot add new partners to the list. It is possible to add only one integration for one partner. The initial design is built for one partner - Google News (https://newsapi.org). News from the configured partners should be shown directly to users and shouldn’t be available among other news to be edited by admin.

## Check list:

  - Verify if UI corresponds to the prototype
  - Admin should be able to configure new partners
  - Admin should be able to view the existing partners’ configurations
  - Admin should be able to edit the existing partners’ configurations
  - Admin should be able to remove integration with partners
  - Integration should be configured only with partners from the predefined list
  - News from configured partners shouldn’t be available in the news list for admin to configure them as articles

## Prototype of the feature

Please click to see the clickable prototypes:
  - [Windows/Linux](https://www.figma.com/proto/1qLqtsJe4qveOaGHay8syy/Manage-News-Partners?page-id=7915%3A851&node-id=7915%3A2024&viewport=266%2C48%2C0.11&scaling=min-zoom&starting-point-node-id=7915%3A2024)
  - [MacOS](https://www.figma.com/proto/1qLqtsJe4qveOaGHay8syy/Manage-News-Partners?page-id=0%3A1073&node-id=0%3A2221&viewport=266%2C48%2C0.03&scaling=scale-down&starting-point-node-id=0%3A2221)

Please click [here](https://www.figma.com/file/1qLqtsJe4qveOaGHay8syy/Manage-News-Partners?node-id=0%3A1073) to see mockups that were included in the prototypes and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure new partners on the portal**](/sports_hub_portal/desktop_application_features/manage_news_partners/user_stories/configure_new_partner)|<pre>As an admin user<br>I want to be able to configure a new integration with a partner<br>So that user will see the news from a third-party source</pre>
2 |[**Allow admin user to activate and deactivate news partners**](/sports_hub_portal/desktop_application_features/manage_news_partners/user_stories/activate_deactivate_partner)|<pre>As an admin user<br>I want to be able to activate or deactivate existing partners</pre>
3 |[**Allow admin user to edit existing partners' configurations on the portal**](/sports_hub_portal/desktop_application_features/manage_news_partners/user_stories/editing_existing_partners_configurations)|<pre>As an admin user<br>I want to be able to change the existing partner's configurations</pre>
4 |[**News from configured partners can not be edited by the admin**](/sports_hub_portal/desktop_application_features/manage_news_partners/user_stories/partners_news_admin_editability)|<pre>As an admin user<br>I should not see the news from the configured partners on the articles list page</pre>
5 |[**Allow admin user to delete the integration with partners on the portal**](/sports_hub_portal/desktop_application_features/manage_news_partners/user_stories/deleting_integration_with_partner)|<pre>As an admin user<br>I want to be able to delete the existing integration with the partner</pre>
