### Back to [Manage news partners on the portal](../../) feature

# Allow admin user to configure new partners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to configure a new integration with a partner
    So that user will see the news from a third-party source

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures a new integration with a partner on the <b>News Partners</b> page</i></b>

Given I am logged in as an admin user

When I view the <b>News Partners</b> page with no partners
Then I see the following:
  - Page headline in the upper-left corner
  - <b>+Add New Partner</b> button in the upper-right corner of the page
  - Empty state message that informs about the absence of integrations with partners with a link for adding the first one

When I click the <b>+Add New Partner</b> button or select the <b>Add New Partner</b> link in the center of the page
Then I see a drop-down list with the available partners on the popover

When I select <b>Google News</b> and click <b>Add</b>
Then I see the new element for inactive <b>Google News</b> integration is added to the list on the <b>News Partners</b> page
  And I see the form with partner-specific boxes is shown:
    - The <b>Cancel</b> button to discard changes and close the form
    - The <b>Save</b> button to save configuration that will be disabled till I make any changes in the form
    - API key –⁠ input for API key provided by Google News after the activation of the development account (mandatory field)
    - Default sources – input for comma-separated sources names, for example, abc-news, associated-press (mandatory field)
    - Section for news sources configuration for all categories with the following:
      - Toggle to configure activation or deactivation
      - Category – the name of the sports category
      - A check box on the left of the <b>Category</b> label
      - Sources – input for comma-separated sources names, for example abc-news, associated-press

When I select the <b>Category</b> check box
Then all categories’ checkboxes are selected/deselected

When I click <b>Cancel</b>
Then I see the confirmation dialog, where I should confirm that I want to leave the form without saving changes

When I click <b>Yes</b>
Then I see that form is closed, changes are not saved, and integration with this partner is inactivated

When I click <b>Save</b>
Then the system saves the changes and displays a message about success

When mandatory fields are not filled
Then I see they are highlighted with red and nothing happens with the form
</pre>

## Mockups

1. Admin user sees the <b>News Partners</b> page with no partners
2. Admin user sees <b>Add New News Partner</b> pop-up window
3. Admin user sees new partner empty form
4. Admin user sees "Something went wrong" error message
5. Admin user sees confirmation pop-up window with the cancelation form

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the News Partners page with no partners:**

![Admin user sees the News Partners page with no partners](/sports_hub_portal/web_application_features/manage_news_partners/images/news_partners_page_with_no_partners.png)

**2. Admin user sees Add New News Partner pop-up window:**

![Admin user sees Add New News Partner pop-up window](/sports_hub_portal/web_application_features/manage_news_partners/images/add_new_news_partners_popup.png)

**3. Admin user sees new partner empty form:**

![Admin user sees new partner empty form](/sports_hub_portal/web_application_features/manage_news_partners/images/add_new_news_partners_empty_form.png)

**4. Admin user sees "Something went wrong" error message:**

![Admin user sees "Something went wrong" error message](/sports_hub_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

**5. Admin user sees confirmation pop-up window with the cancelation form:**

![Admin user sees confirmation pop-up window with the cancelation form](/sports_hub_portal/web_application_features/manage_news_partners/images/cancel_confirmation_popup.png)

</details>

## Test cases

1. Verify the possibility to add new partners from the predefined list with all valid data
2. Verify the possibility to cancel adding of new partners from a predefined list
3. Verify that it is not possible to save new partners with empty mandatory fields

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to add new partners from the predefined list with all valid data**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page|1) Click <b>+ Add New Partner</b></br>2) Select the partner from the drop-down list</br>3) Click <b>Add</b></br>4) In the <b>API key</b> and <b>Default sources</b> inputs, enter valid data</br>5) Check some categories</br>6) Click <b>Save</b>|1) The form to add a new news partner appears with a predefined list of partners</br>3) The partner is added as inactive into the list with all empty boxes</br>6) A notification about successful saving of changes appears, the new partner is saved with inactive state, and news is loaded from the source. The partner is not available to be added twice (not present in the drop-down list)|

### **#2. Verify the possibility to cancel adding of new partners from a predefined list**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page|1) Click <b>+ Add New Partner</b></br>2) Click <b>Cancel</b></br>3) Click <b>+ Add New Partner</b></br>4) Select the partner from the drop-down list</br>5) Click <b>Add</b></br>6) In the <b>API key</b> and <b>Default sources</b> inputs, enter valid data</br>7) Check categories</br>8) Click <b>Cancel</b></br>9) Click <b>Yes</b>|1) The form to add a new news partner appears with a predefined list of partners in the drop-down list</br>2) The form is closed and the partner is not added</br>3) The <b>Add new News partner</b> popover appears with a predefined list of partners in the drop-down list</br>5) The partner is added as inactive into the list with all empty fields</br>8) Popover with a warning about missing changes appears</br>9) Changes to the news partner are not saved|

### **#3. Verify that it is not possible to save new partners with empty mandatory fields**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page|1) Click <b>+ Add New Partner</b></br>2) Select the partner from the drop-down list</br>3) Click <b>Add</b></br>4) Do not fill in the API key box</br>5) In the Default sources box, enter valid data</br>6) Click <b>Save</b></br>7) In the <b>API key</b> input, enter valid data</br>8) Do not fill in the <b>Default sources</b> input</br>9) Click <b>Save</b>|1) The <b>Add new News partner</b> popover appears with a predefined list of partners in the drop-down list</br>3) The partner is added as inactive into the list with all empty boxes</br>6) Warning message about required fields appears. The partner is not saved</br>9) Warning message about required fields appears. The partner is not saved|
</details>
