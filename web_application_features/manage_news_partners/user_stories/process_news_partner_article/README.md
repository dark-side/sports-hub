### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to process news from partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to process news from partners
    So that they are published and visible for the site users

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is processing the article from the news partners</i></b>

Given I am logged in as an admin user

When I am on the <b>Edit</b> tab of the <b>News Partners</b> page
Then I see a drop-down with two statuses <b>Draft</b> and <b>Ready for processing</b>
  And <b>Draft</b> is selected by default

When I finished updating the article and filling out all the required fields
Then I click <b>Save</b> button

When I select <b>Ready for processing</b> status in the drop-down
Then the article is moved to <b>Ready for processing</b>

When article is in <b>Ready for processing</b> status
Then I am not allowed to edit the article and change status back to <b>Draft</b>
  And <b>Save</b> and <b>Cancel</b> buttons are disabled

When there is at least one article in <b>Ready for processing</b> status
<b>Then the background job picks these articles and moves them to the main database to the table with articles created by the admin user
  And the background job runs every hour

When the background job processed and copied the article to the main database
Then the article status is changed to <b>Precessed</b>
  And article status in the main database is <b>Published</b>
</b>

When article is in <b>Processed</b> status
Then I am not allowed to edit the article and change status back to <b>Draft</b>
  And <b>Save</b> and <b>Cancel</b> buttons are disabled

When I view the <b>News Partners</b> page and click <b>News</b> tab
Then I see a list of articles from the partners

When I hover over an article in <b>Draft</b> status
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click the "<b>...</b>" menu icon
Then I see the following options:
  - <b>Edit</b>
  - <b>Delete</b>
  - <b>Ready for processing</b>

When I select <b>Ready for processing</b> in the menu
Then the article is moved to <b>Ready for processing</b>

When I hover over an article in <b>Ready for processing</b> status
Then I do not see the ellipsis (<b>...</b>) button

When I hover over an article in <b>Processed</b> status
Then I do not see the ellipsis (<b>...</b>) button
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the status drop-down on the <b>Edit</b> partner article tab
2. Admin user clicks the status drop-down on the <b>Edit</b> partner article tab
3. Admin user sees the <b>Ready for processing</b> in the drop-down after selecting it and disabled <b>Save</b> and <b>Cancel</b> buttons
4. Admin user sees the <b>Processing</b> intead of the drop-down after the background job started process and disabled <b>Save</b> and <b>Cancel</b> buttons
5. Admin user sees the <b>Processed</b> intead of the drop-down after the background job finished process it and disabled <b>Save</b> and <b>Cancel</b> buttons
6. Admin user sees the article in <b>Ready for processing</b> status on the <b>News Partners</b> page
7. Admin user hovers over the article and sees the ellipsis (<b>...</b>) button
8. Admin user hovers over the article, clicks the ellipsis (<b>...</b>) button, and sees action list

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the status drop-down on the Edit partner article tab:**

![Admin user sees the status drop-down on the Edit partner article tab](/web_application_features/manage_news_partners/images/status_dropdown_on_edit_page.png)

**2. Admin user clicks the status drop-down on the Edit partner article tab:**

![Admin user clicks the status drop-down on the Edit partner article tab](/web_application_features/manage_news_partners/images/click_status_dropdown_on_edit_page.png)

**3. Admin user sees the Ready for processing in the drop-down after selecting it and disabled Save and Cancel buttons:**

![Admin user sees the Ready for processing in the drop-down after selecting it and disabled Save and Cancel buttons](/web_application_features/manage_news_partners/images/click_status_dropdown_on_edit_page_ready_for_processing.png)

**4. Admin user sees the Processing intead of the drop-down after the background job started process and disabled Save and Cancel buttons:**

![Admin user sees the Processing intead of the drop-down after the background job started process and disabled Save and Cancel buttons](/web_application_features/manage_news_partners/images/processing_status_on_edit_page.png)

**5. Admin user sees the Processed intead of the drop-down after the background job finished process it and disabled Save and Cancel buttons:**

![Admin user sees the Processed intead of the drop-down after the background job finished process it and disabled Save and Cancel buttons](/web_application_features/manage_news_partners/images/processed_status_on_edit_page.png)

**6. Admin user sees the article in Ready for processing status on the News Partners page:**

![Admin user sees the article in Ready for processing status on the News Partners page](/web_application_features/manage_news_partners/images/news_partner_list_page_ready_for_processing.png)

**7. Admin user hovers over the article and sees the ellipsis (...) button:**

![Admin user hovers over the article and sees the ellipsis (...) button](/web_application_features/manage_news_partners/images/admin_hovers_over_article.png)

**8. Admin user hovers over the article, clicks the ellipsis (...) button, and sees action list:**

![Admin user hovers over the article, clicks the ellipsis (...) button, and sees action list](/web_application_features/manage_news_partners/images/admin_clicks_ellipsis_button.png)

</details>

## Test cases

1. Verify that the article goes to <b>Ready for processing</b> status when an admin user selects <b>Ready for processing</b> on the <b>Edit</b> article tab
2. Verify that the article goes to <b>Ready for processing</b> status when an admin user selects <b>Ready for processing</b> on the on the <b>News Partners</b> page
3. Verify that the article goes to <b>Processed</b> status and is moved to the main database with <b>Published</b> status when the background job processed the articles that have <b>Ready for processing</b> status
4. Verify that the admin user does not see the ellipsis (<b>...</b>) menu button on the <b>News</b> tab for the article in <b>Ready for processing</b>
5. Verify that the admin user can not edit the article in <b>Ready for processing</b> and <b>Processed</b> status

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the article goes to Ready for processing status when an admin user selects Ready for processing on the Edit article tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Go to edit some draft articles</br>4) Select <b>Ready for processing</b> status in the drop-down</br>5) Observe the page</br>6) Check article status|5) The <b>Save</b> and <b>Cancel</b> buttons are disabled. Status drop-down is disabled</br>6) Article status is <b>Ready for processing</b>|

### **#2. Verify that the article goes to Ready for processing status when an admin user selects Ready for processing on the on the News Partners page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some draft articles</br>4) Hover over the draft article</br>5) Click the ellipsis (<b>...</b>) menu button and select <b>Ready for processing</b> option</br>6) Check article status|6) Article status is <b>Ready for processing</b>|

### **#3. Verify that the article goes to Processed status and is moved to the main database with Published status when the background job processed the articles that have Ready for processing status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some articles in <b>Ready for processing</b> status</br>4) Wait for the background job to finish run</br>5) Check article status</br>6) Check article status in the main database|5) The article is in <b>Processed</b> status</br>6) The article is in <b>Published</b> status|

### **#4. Verify that the admin user does not see the ellipsis (...) menu button on the News tab for the article in Ready for processing**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some <b>Ready for processing</b> article</br>4) Hover over that article</br>5) Observe the page|6) The ellipsis (<b>...</b>) menu button is not visible for the article in <b>Ready for processing</b> status|

### **#5. Verify that the admin user can not edit the article in Ready for processing and Processed status**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some <b>Ready for processing</b> and <b>Processed</b> articles</br>4) Hover over <b>Ready for processing</b> article</br>5) Hover over <b>Processed</b> article</br>6) Go to <b>Edit</b> tab for <b>Processed</b> article</br>7) Go to <b>Edit</b> tab for  <b>Processed</b> article|4) The ellipsis (<b>...</b>) menu button is not visible for the article</br>5) The ellipsis (<b>...</b>) menu button is not visible for the article</br>6) - 7) The <b>Save</b> and <b>Cancel</b> buttons are disabled|

</details>
