### Back to [Manage News Partners on the portal](../../) feature

# Allow admin user to activate/deactivate news partners

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to activate or deactivate existing partners

## Acceptance criteria

<pre>
Scenario: An admin user views the list of existing partners configurations on the News Partners page
Given I am logged in as an admin user

When I view the <b>News Partners</b> page where at least one partner was added
Then I see the list with one item per one partner
  And I see that each item has:
    -  Plus/minus icon on the left side to open/close the form
    - Partner's name right after the plus/minus icon
    - Toggle to activate/deactivate the integration 
    - Edit icon
    - Delete icon

When I switch toggle and deactivate integration
Then I see a confirmation popover, where I should confirm that I want to deactivate the partner

When I click <b>Yes</b>
Then I see that partner is deactivated

When I switch the toggle to activate the integration and mandatory boxes are filled
Then I see that partner is activated

When I switch the toggle to activate the integration and mandatory boxes are not filled
Then I see the form is opened and the required boxes are highlighted with red color
</pre>

## Mockups

1. Admin user sees News Partners list
2. Admin user sees new/edit news partner form
3. Admin user sees "Something went wrong" message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![Admin user sees News Partners list](/products/sport_news_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees new/edit news partner form:**

![Admin user sees new/edit news partner form](/products/sport_news_portal/web_application_features/manage_news_partners/images/new_news_partners_edit_state.png)

**3. Admin user sees "Something went wrong" message:**

![Admin user sees "Something went wrong" message](/products/sport_news_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test cases

1. Verify the possibility to deactivate integration with news partner
2. Verify the possibility to activate integration with news partner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to deactivate integration with news partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added in the active state|1) Switch the active toggle</br>2) Click <b>Yes</b>|1) The confirmation popover about deactivation appears</br>2) Partner is the inactive state. No new news are loaded from the partner to the site|

### **#2. Verify the possibility to activate integration with news partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added in the inactive state|1) Switch the inactive toggle</br>2) Click <b>Yes</b>|1) The confirmation message about activation appears</br>2) Partner is the active state. New news are loaded from the partner to the site|
</details>
