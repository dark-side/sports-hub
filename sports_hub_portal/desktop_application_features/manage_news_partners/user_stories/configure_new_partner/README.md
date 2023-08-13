### Back to [Manage news partners on the portal](../../README.md) feature

# Allow admin user to configure new partners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Style guides](#style-guides)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to configure a new integration with a partner

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user configures a new integration with a partner on the <b>News Partners</b> page</i></b>

Given I am logged in as an admin user

When I view the <b>News Partners</b> page with no partners
Then I see the following:
  - Page headline in the upper-left corner
  - <b>Partners</b> tab is active
  - <b>News</b> tab
  - Empty state message that informs about the absence of integrations with partners

When news partners names are seeded to the database (for example, <b>Google News</b>)
Then I see a list of those partners on the <b>News Partners</b> page
  And all partners are inactive by default

When I click <b>Google News</b>
Then I see the form with partner-specific boxes is shown:
  - The <b>Cancel</b> button to discard changes and close the form
  - The <b>Save</b> button to save configuration that will be disabled till I make any changes in the form
  - API key – input for API key provided by Google News after the activation of the development account (mandatory field)
  - Default sources – input for comma-separated sources names, for example, abc-news, associated-press (mandatory field)

When I click <b>Cancel</b>
Then I see that form is closed, changes are not saved, and integration with this partner is inactivated

When I click <b>Save</b>
Then the system saves the changes and displays a message about success

When mandatory fields are not filled
Then I see they are highlighted with red and nothing happens with the form

<i>NOTE: Admin should not have ability to delete the partner through the UI. They should only deactivate it.</i>
</pre>

## Style guides

Follow [a link](https://www.figma.com/proto/0zkkf5WC77OSpvyD6YXpFE/Style-guides?page-id=0%3A1&node-id=19%3A5368&viewport=266%2C48%2C0.54&scaling=min-zoom&starting-point-node-id=19%3A5368) to the style guides

## Mockups

1. Admin user sees the <b>News Partners</b> page with no partners
2. Admin user sees a list of partners
3. Admin user sees new partner empty form
4. Admin user sees new partner filled in form
5. Admin user sees "Something went wrong" error message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees the News Partners page with no partners:**

![Admin user sees the News Partners page with no partners](/sports_hub_portal/desktop_application_features/manage_news_partners/images/news_partners_page_with_no_partners.png)

**2. Admin user sees a list of partners:**

![Admin user sees a list of partners](/sports_hub_portal/desktop_application_features/manage_news_partners/images/news_partners_list.png)

**3. Admin user sees new partner empty form:**

![Admin user sees new partner empty form](/sports_hub_portal/desktop_application_features/manage_news_partners/images/news_partners_empty_form.png)

**4. Admin user sees new partner filled in form:**

![Admin user sees new partner filled in form](/sports_hub_portal/desktop_application_features/manage_news_partners/images/news_partners_filled_form.png)

**5. Admin user sees "Something went wrong" error message:**

![Admin user sees "Something went wrong" error message](/sports_hub_portal/desktop_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test cases

1. Verify new partners are seeded and visible on the <b>News Partners</b> configuration page
2. Verify the possibility to cancel adding of new partners from a predefined list
3. Verify that it is not possible to save new partners with empty mandatory fields

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify new partners are seeded and visible on the News Partners configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Partners are seeded successfully</br>- Log in with admin account|1) Go to the <b>News Partners</b> configuration page</br>2) Select the partner from the avaliable list</br>3) In the <b>API key</b> and <b>Default sources</b> inputs, enter valid data</br>4) Click <b>Save</b>|1) The partners are added as inactive into the list with all empty settings</br>4) A notification about successful saving of changes appears, the new partner is saved with inactive state|

### **#2. Verify the possibility to cancel adding of new partners from a predefined list**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page|1) Select the partner from the avaliable list</br>2) In the <b>API key</b> and <b>Default sources</b> inputs, enter valid data</br></br>3) Click <b>Cancel</b>|3) Changes to the news partner are not saved|

### **#3. Verify that it is not possible to save new partners with empty mandatory fields**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page|1) Select the partner from the avaliable list</br>2) Do not fill in the API key input</br>3) In the Default sources input, enter valid data</br>4) Click <b>Save</b></br>5) In the <b>API key</b> input, enter valid data</br>6) Do not fill in the <b>Default sources</b> input</br>7) Click <b>Save</b>|4) Warning message about required fields appears. The partner is not saved</br>7) Warning message about required fields appears. The partner is not saved|
</details>
