### Back to [Web site](../../#web-site) functional requirements

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
  - Users should be able to view the news from configured partners

## Prototype of the feature

Please click [here](https://www.figma.com/proto/U7MdkpMsV1yimaWduSnzZP/Manage-News-Partners?node-id=6615%3A14257&viewport=-223%2C371%2C0.02814709022641182&scaling=scale-down) to see a clickable prototype.

Please click [here](https://www.figma.com/file/U7MdkpMsV1yimaWduSnzZP/Manage-News-Partners?node-id=0%3A1073) to see mockups that were included in the prototype and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure new partners on the portal**](/sports_hub_portal/web_application_features/manage_news_partners/user_stories/configure_new_partner)|<pre>As an admin user<br>I want to be able to configure a new integration with a partner<br>So that user will see the news from a third-party source</pre>
2 |[**Allow admin user to activate and deactivate news partners**](/sports_hub_portal/web_application_features/manage_news_partners/user_stories/activate_deactivate_partner)|<pre>As an admin user<br>I want to be able to activate or deactivate existing partners</pre>
3 |[**Allow admin user to edit existing partners' configurations on the portal**](/sports_hub_portal/web_application_features/manage_news_partners/user_stories/editing_existing_partners_configurations)|<pre>As an admin user<br>I want to be able to change the existing partner's configurations</pre>
4 |[**News from configured partners can not be edited by the admin**](/sports_hub_portal/web_application_features/manage_news_partners/user_stories/partners_news_admin_editability)|<pre>As an admin user<br>I should not see the news from the configured partners on the articles list page</pre>
5 |[**Allow admin user to delete the integration with partners on the portal**](/sports_hub_portal/web_application_features/manage_news_partners/user_stories/deleting_integration_with_partner)|<pre>As an admin user<br>I want to be able to delete the existing integration with the partner</pre>
6 |[**Allow site users to view news from configured partners**](/sports_hub_portal/web_application_features/manage_news_partners/user_stories/viewing_news_from_partners)|<pre>As a site user<br>I want to be able to see the news from configured partners in the appropriate categories</pre>
