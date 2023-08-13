### Back to [Website](/web_application_features/web_application_features_list/README.md) functional requirements

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

Integration can be configured only with partners from the predefined list.
Admin cannot add new partners to the list. It is possible to add only one integration for one partner. The initial design is built for one partner - Google News (https://newsapi.org). News from the configured partners should be shown directly to users and shouldn’t be available among other news to be edited by admin.

When the partner is configured and activated, the raw articles should be saved to a separate database in Draft status for further review by the admin user. The admin user should be able to see raw article data and be able to update the article, fill out all missing information, set the category, subcategory, team, etc. After the updated information is saved, the admin user should be able to move those articles to <b>Ready for processing</b> status. Then the background job should run every hour and pick all articles in <b>Ready for processing</b> status and move them to the main database and save them to a general articles table in <b>Published</b> status. The background job should update the status from <b>Ready for processing</b> to <b>Processed</b> after the article was moved to the main database.

## Check list:

  - Verify if UI corresponds to the prototype
  - Admin should be able to configure new partners
  - Admin should be able to view the existing partners’ configurations
  - Admin should be able to edit the existing partners’ configurations
  - Admin should not be able to remove integration with partners
  - Integration should be configured only with partners from the predefined list
  - Admin should be able to edit the raw articles from the news partner
  - Admin should be able to process and publish the raw articles from the news partner
  - Users should be able to view the news from configured partners

## Prototype of the feature

Please click [here](https://www.figma.com/proto/U7MdkpMsV1yimaWduSnzZP/Manage-News-Partners?page-id=7917%3A851&node-id=7922%3A3319&viewport=266%2C48%2C0.09&scaling=min-zoom&starting-point-node-id=7934%3A2313&show-proto-sidebar=1) to see a clickable prototype.

Please click [here](https://www.figma.com/file/U7MdkpMsV1yimaWduSnzZP/Manage-News-Partners?node-id=7917%3A851) to see mockups that were included in the prototype and additional style guides.

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## User stories

No           |      Name     |   Details
------------ | ------------- | -------------
1 |[**Allow admin user to configure new partners on the portal**](/web_application_features/manage_news_partners/user_stories/configure_new_partner/README.md)|<pre>As an admin user<br>I want to be able to configure a new integration with a partner</pre>
2 |[**Allow admin user to edit existing partners' configurations on the portal**](/web_application_features/manage_news_partners/user_stories/edit_existing_partners_configurations/README.md)|<pre>As an admin user<br>I want to be able to change the existing partner's configurations</pre>
3 |[**Allow admin user to activate and deactivate news partners**](/web_application_features/manage_news_partners/user_stories/activate_deactivate_partner/README.md)|<pre>As an admin user<br>I want to be able to activate or deactivate existing partners</pre>
4 |[**Allow admin user to see a list of news from partners**](/web_application_features/manage_news_partners/user_stories/partner_news_list/README.md)|<pre>As an admin user<br>I want to see a list of news from partners</pre>
5 |[**Allow admin user to filter a list of news from partners**](/web_application_features/manage_news_partners/user_stories/filter_partner_news_list/README.md)|<pre>As an admin user<br>I want to be able to filter a list of news from partners</pre>
6 |[**Allow admin user to edit news from partners**](/web_application_features/manage_news_partners/user_stories/edit_articles_from_news_partners/README.md)|<pre>As an admin user<br>I want to be able to edit news from partners</pre>
7 |[**Allow admin user to delete news from partners**](/web_application_features/manage_news_partners/user_stories/delete_articles_from_news_partners/README.md)|<pre>As an admin user<br>I want to be able to delete news from partners</pre>
8 |[**Allow admin user to process news from partners**](/web_application_features/manage_news_partners/user_stories/process_news_partner_article/README.md)|<pre>As an admin user<br>I want to be able to process news from partners<br>So that they are published and visible for the site users</pre>
9 |[**Allow admin user to see articles from configured partners on the articles list page**](/web_application_features/manage_news_partners/user_stories/partners_news_admin_editability/README.md)|<pre>As an admin user<br>I want to see articles from the news partners on the articles list page after they are processed</pre>
10 |[**Allow site users to view news from configured partners**](/web_application_features/manage_news_partners/user_stories/viewing_news_from_partners/README.md)|<pre>As a site user<br>I want to be able to see the news from configured partners in the appropriate categories</pre>
