### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to edit news from partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to edit news from partners

## Acceptance criteria

<pre>
<b><i>Scenario: An admin is editing the article from the news partners</i></b>

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

When I click <b>Edit</b>
Then I am redirected to the article view page
  And I see a house icon that routes to the <b>News</b> tab
  And the article healdile
  And I see two tabs:
    - <b>Original</b>
    - <b>Edit</b>
  And <b>Edit</b> is an active tab

When I view the <b>News Partners</b> page and click <b>News</b> tab
  And select an article from the list
Then I am redirected to the article view page
  And I see a house icon that routes to the <b>News</b> tab
  And the article healdile
  And I see two tabs:
    - <b>Original</b>
    - <b>Edit</b>
  And <b>Original</b> is an active tab

When I am on the <b>Original</b>
Then I always see original article details: image, alt., headline, content
  And all fields are disabled

When I am on the <b>Edit</b>
Then I see original article details: image, alt., headline, content
  And all fields are editable
  And I see:
  - <b>Cancel</b> and <b>Save</b> buttons
  - Page languages
  - a drop-down to change the article status

When I change some field and click <b>Save</b>
Then I see a notification message about success
  And all changes are saved

When I change some field and click <b>Cancel</b>
Then the confirmation popover appears

When I confirm cancelation on the popover
Then I see all changes are discarded
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>Original</b> tab
2. Admin user sees the <b>Edit</b> tab
3. Admin user sees a notification message about success
4. Admin user sees the confirmation popover on cancel

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the Original tab:**

![Admin user sees the Original tab](/desktop_application_features/manage_news_partners/images/partner_news_original_tab.png)

**2. Admin user sees the Edit tab:**

![Admin user sees the Edit tab](/desktop_application_features/manage_news_partners/images/partner_news_edit_tab.png)

**3. Admin user sees a notification message about success:**

![Admin user sees a notification message about success](/desktop_application_features/manage_news_partners/images/partner_news_edit_tab_success_save.png)

**4. Admin user sees the confirmation popover on cancel:**

![Admin user sees the confirmation popover on cancel](/desktop_application_features/manage_news_partners/images/partner_news_edit_tab_cancel_confirmation.png)
</details>

## Test cases

1. Verify that the admin user is taken to the <b>Original</b> tab when clicking on the article on the <b>News</b> tab
2. Verify that the admin user is taken to the <b>Edit</b> tab when selecting the <b>Edit</b> option in the ellipsis (<b>...</b>) menu button on the <b>News</b> tab
3. Verify that changes are saved when the admin user clicks the <b>Save</b> button
4. Verify that changes are discarded when the admin user clicks the <b>Cancel</b> button

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that the admin user is taken to the Original tab when clicking on the article on the News tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some draft articles</br>4) Select article|4) The user is redirected to the <b>Original</b> tab of the selected article|

### **#2. Verify that the admin user is taken to the Edit tab when selecting the Edit option in the ellipsis (...) menu button on the News tab**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some draft articles</br>4) Hover over the draft article</br>5) Click the ellipsis (<b>...</b>) menu button and select <b>Edit</b> option|4) The user is redirected to the <b>Edit</b> tab of the selected article|

### **#3. Verify that changes are saved when the admin user clicks the Save button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some draft articles</br>4) Go to the <b>Edit</b> page of the selected article</br>4) Change any field</br>5) Click the <b>Save</b> button|5) The changes are saved and user sees a notification message about success|

### **#4. Verify that changes are discarded when the admin user clicks the Cancel button**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Logged in with admin account</br>- There is some partner added|1) Go to the <b>News Partners</b> list page</br>2) Click <b>News</b> tab</br>3) Have some draft articles</br>4) Go to the <b>Edit</b> page of the selected article</br>4) Change any field</br>5) Click the <b>Cancel</b> button</br>6) Confirn cancelation|5) The confirmation popover appears</br>6) The changes are discarded|
</details>
