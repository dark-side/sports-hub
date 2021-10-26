### Back to [Manage news partners on the portal](../../) feature

# Allow admin user to delete the integration with partners on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete the existing integration with the partner

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes the existing integration with the partner on the <b>News Partners</b> page</i></b>

Given I am logged in as an admin user

When I click the Delete icon for the needed partner on the <b>News Partners</b> page
Then I see a confirmation pop-up window "Are you sure you want to delete the integration with {partner's name}?"

When I click <b>Cancel</b>
Then I see the pop-up window disappears and nothing changes

When I click <b>Yes</b>
Then I see a notification message about success
  And I see the updated list
</pre>

## Mockups

1. Admin user sees <b>News Partners</b> list
2. Admin user sees a confirmation pop-up window to delete partner integration
3. Admin user sees "Something went wrong" error message

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![Admin user sees News Partners list](/products/sports_hub_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees a confirmation pop-up window to delete partner integration:**

![Admin user sees a confirmation pop-up window to delete partner integration](/products/sports_hub_portal/web_application_features/manage_news_partners/images/delete_news_partner_warning_popup.png)

**3. Admin user sees "Something went wrong" error message:**

![Admin user sees "Something went wrong" error message](/products/sports_hub_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test cases

1. Verify the possibility to delete partner integration
2. Verify the possibility to cancel deleting of the partner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to delete partner integration**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) In the partner row, click the Delete icon</br>2) Click <b>Delete</b>|1) Popover to confirm deleting appears</br>2) The news partner is removed from the list. Users can add new partners in the drop-down list again|

### **#2. Verify the possibility to cancel deleting of the partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) In the partner row, click the Delete icon</br>2) Click <b>Cancel</b>|1) Popover to confirm deleting appears</br>2) The news partner is still present|
</details>
