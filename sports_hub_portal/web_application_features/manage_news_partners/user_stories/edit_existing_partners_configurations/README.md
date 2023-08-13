### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to edit existing partners' configurations on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to change the existing partner's configurations

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user changes the existing partner's configurations on the News Partners page</i></b>

Given I am logged in as an admin user

When I click the Plus icon for the needed partner on the <b>News Partners</b> page
Then I see the edit form with pre-filled configurations below the row for the needed partner in the list

When I click <b>Cancel</b>
Then I see that form is closed and no changes were saved

When I click <b>Save</b>
Then the system saves the changes and displays a message about success
  And I see the list of existing partners
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees <b>News Partners</b> list
2. Admin user sees new/edit news partner form
3. Admin user sees "Something went wrong" error message
4. Admin user sees confirmation pop-up window on the cancelation form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![Admin user sees News Partners list](/sports_hub_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees new/edit news partner form:**

![Admin user sees new/edit news partner form](/sports_hub_portal/web_application_features/manage_news_partners/images/new_news_partners_edit_state.png)

**3. Admin user sees "Something went wrong" error message:**

![Admin user sees "Something went wrong" error message](/sports_hub_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

**4. Admin user sees confirmation pop-up window on the cancelation form:**

![Admin user sees confirmation pop-up window on the cancelation form](/sports_hub_portal/web_application_features/manage_news_partners/images/cancel_confirmation_popup.png)

</details>

## Test cases

1. Verify the possibility to edit the partner with all valid data
2. Verify the possibility to cancel editing of the partner
3. Verify that it is not possible to save the edited partner with empty mandatory boxes

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to edit the partner with all valid data**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) Select a partner, and then click <b>Expand</b> (+)</br>2) In the <b>Default sources</b> and <b>API key</b> inputs, enter valid data</br>3) Select and unselect some categories checkboxes</br>4) Click <b>Save</b>|1) The boxes for the selected partner are available for editing</br>4) A notification about successful saving of changes appears, news partner is saved in the previous state, and news is loaded from the source according to changed data|

### **#2. Verify the possibility to cancel editing of the partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) Select a partner, and then click <b>Expand</b> (+)</br>2) In the <b>Default sources</b> and <b>API key</b> inputs, enter valid data</br>3) Select and unselect some categories check boxes</br>4) Click <b>Cancel</b></br>5) Click <b>Yes</b>|1) The boxes for the selected partner are available for editing</br>4) Popover with warning about missing changes appears</br>5) Changes to the <b>News Partners</b> page are not saved|

### **#3. Verify that it is not possible to save the edited partner with empty mandatory boxes**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) Select a partner, and then click <b>Expand</b> (+)</br>2) In the <b>API key</b> input, delete data</br>3) Click <b>Save</b></br>4) In the <b>API key</b> input, enter valid data</br>5) In the <b>Default sources</b> input, delete data</br>6) Click <b>Save</b>|1) The boxes for the selected partner are available for editing</br>3) Warning message about required boxes appears. The partner is not saved</br>6) Warning message about required boxes appears. The partner is not saved|
</details>
