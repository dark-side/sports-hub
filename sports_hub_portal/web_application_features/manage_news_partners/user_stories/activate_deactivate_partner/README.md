### Back to [Manage news partners on the portal](../../) feature

# Allow admin user to activate and deactivate news partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
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
    - The Edit icon
    - The Delete icon

When I switch toggle and deactivate integration
Then I see a confirmation popover, where I should confirm that I want to deactivate the partner

When I click <b>Yes</b>
Then I see that partner is deactivated

When I switch the toggle to activate the integration and mandatory boxes are filled
Then I see that partner is activated

When I switch the toggle to activate the integration and mandatory boxes are not filled
Then I see the form is opened and the required boxes are highlighted with red
</pre>

## Mockups

1. Admin user sees <b>News Partners</b> list
2. Admin user sees new/edit news partner form
3. Admin user sees "Something went wrong" error message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![Admin user sees News Partners list](/sports_hub_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees new/edit news partner form:**

![Admin user sees new/edit news partner form](/sports_hub_portal/web_application_features/manage_news_partners/images/new_news_partners_edit_state.png)

**3. Admin user sees "Something went wrong" error message:**

![Admin user sees "Something went wrong" error message](/sports_hub_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test cases

1. Verify the possibility to deactivate integration with news partner
2. Verify the possibility to activate integration with news partner

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
</details>
