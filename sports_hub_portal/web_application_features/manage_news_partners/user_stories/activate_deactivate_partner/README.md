### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to activate and deactivate news partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to activate or deactivate existing partners

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user views the list of existing partners configurations on the News Partners page</i></b>

Given I am logged in as an admin user

When I view the <b>News Partners</b> page where at least one partner was added
Then I see the list with one item per one partner
  And I see that each item has:
    - Plus and Minus icons on the left side to open/close the form
    - Partner's name right after Plus and Minus icons
    - The toggle to activate or deactivate the integration

When I switch toggle and deactivate integration
Then I see a confirmation popover, where I should confirm that I want to deactivate the partner

When I click <b>Yes</b>
Then I see that partner is deactivated

When I switch the toggle to activate the integration and mandatory boxes are filled
Then I see that partner is activated

When I switch the toggle to activate the integration and mandatory boxes are not filled
Then I see the form is opened and the required boxes are highlighted with red

When I the integration has at least one empty setting (<b>API key</b> and/or <b>Default sources</b>)
  And I hover over the toggle
Then I see <b>Inactive</b> toggle is disabled and a hover popup displays a message: "You can not activate the partner. Please fill in the settings."

When the partner is activated
Then there is a background job that pulls the news every hour
  And saves the raw articles to a separate database for further review

<i>NOTE: Admin should not have ability to delete the partner through the UI. They should only deactivate it.</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>News Partners</b> list
2. Admin user sees new/edit news partner form
3. Admin user sees a message on hover over partner with empty settings
4. Admin user sees "Something went wrong" error message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![Admin user sees News Partners list](/sports_hub_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees new/edit news partner form:**

![Admin user sees new/edit news partner form](/sports_hub_portal/web_application_features/manage_news_partners/images/new_news_partners_edit_state.png)

**3. Admin user sees a message on hover over partner with empty settings:**

![Admin user sees a message on hover over partner with empty settings](/sports_hub_portal/web_application_features/manage_news_partners/images/inactive_empty_partner_hover.png)

**4. Admin user sees "Something went wrong" error message:**

![Admin user sees "Something went wrong" error message](/sports_hub_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)
</details>

## Test cases

1. Verify the possibility to deactivate integration with news partner
2. Verify the possibility to activate integration with news partner
3. Verify that the raw articles are pulled from the news partner to a separate database for further review

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to deactivate integration with news partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added in the active state|1) Switch the active toggle</br>2) Click <b>Yes</b>|1) The confirmation popover about deactivation appears</br>2) Partner is in the inactive state. No new news is loaded from the partner to the site|

### **#2. Verify the possibility to activate integration with news partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added in the inactive state|1) Switch the inactive toggle</br>2) Click <b>Yes</b>|1) The confirmation message about activation appears</br>2) Partner is in the active state. New news is loaded from the partner to the site|

### **#3. Verify that the raw articles are pulled from the news partner to a separate database for further review**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added in the active state|1) Wait for 1 hour after activating the partner</br>2) Check the database|1) The background job runs every hour</br>2) The raw articles from the news partner are saved into separate database|
</details>
