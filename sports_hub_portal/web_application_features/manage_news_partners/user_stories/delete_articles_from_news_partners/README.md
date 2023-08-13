### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to delete news from partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete news from partners

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is deleting the article from the news partners</i></b>

Given I am logged in as an admin user

When I view the <b>News Partners</b> page and click <b>News</b> tab
Then I see a list of articles from the partners

When I hover over an article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner
  And the ellipsis (<b>...</b>) button is available only for <b>Draft</b> articles

When I click the "<b>...</b>" menu icon
Then I see the following options:
  - <b>Edit</b>
  - <b>Delete</b>
  - <b>Ready for processing</b>

When I click <b>Delete</b>
Then the confirmation popover appears

When I confirm cancelation on the popover
Then I see the selected article is deleted from the list
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees articles list
2. Admin user hovers over the article and sees the ellipsis (<b>...</b>) button
3. Admin user hovers over the article, clicks the ellipsis (<b>...</b>) button, and sees action list
4. Admin user sees the confirmation popover on delete
5. Admin user sees a notification message about success

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees articles list:**

![Admin user sees articles list](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_side_partner_articles_list.png)

**2. Admin user hovers over the article and sees the ellipsis (...) button:**

![Admin user hovers over the article and sees the ellipsis (...) button](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_hovers_over_article.png)

**3. Admin user hovers over the article, clicks the ellipsis (...) button, and sees action list:**

![Admin user hovers over the article, clicks the ellipsis (...) button, and sees action list](/sports_hub_portal/web_application_features/manage_news_partners/images/admin_clicks_ellipsis_button.png)

**4. Admin user sees the confirmation popover on delete:**

![Admin user sees the confirmation popover on delete](/sports_hub_portal/web_application_features/manage_news_partners/images/partner_news_edit_tab_delete_confirmation.png)

**5. Admin user sees a notification message about success:**

![Admin user sees a notification message about success](/sports_hub_portal/web_application_features/manage_news_partners/images/partner_news_success_delete.png)
</details>

## Test cases

1. Verify that the admin user can delete a draft article from the news partner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the admin user can delete a draft article from the news partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some draft articles</br>4) Hover over the draft article</br>5) Click the ellipsis (<b>...</b>) menu button and select <b>Delete</b> option</br>6) Confirm deletion on the confirmation popover|5) The confirmation popover</br>6) The confirmation popover dissapers and a success notification appears|
</details>
