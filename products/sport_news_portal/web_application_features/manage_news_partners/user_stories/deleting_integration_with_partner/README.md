### Back to [Manage News Partners on the portal](../../) feature

# Allow admin user to delete the integration with the partner on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to be able to delete the existing integration with the partner

## Acceptance criteria

<pre>
Scenario: An admin user deletes the existing integration with the partner on the News Partners page
Given I am logged in as an admin user

When I click the delete icon for the needed partner on the <b>News Partners</b> page
Then I see a confirmation popup "Are you sure you want to delete the integration with {partner name}?"

When I click <b>Cancel</b>
Then I see the popover disappears and nothing changes

When I click <b>Yes</b>
Then I see a notification message about success
  And I see the updated list
</pre>

## Mockups

1. Admin user sees News Partners list
2. Admin user sees a confirmation popup on delete
3. Admin user sees “Something went wrong” popup

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees News Partners list:**

![Admin user sees News Partners list](/products/sport_news_portal/web_application_features/manage_news_partners/images/news_partners_list.png)

**2. Admin user sees a confirmation popup on delete:**

![Admin user sees a confirmation popup on delete](/products/sport_news_portal/web_application_features/manage_news_partners/images/delete_news_partner_warning_popup.png)

**3. Admin user sees "Something went wrong" message:**

![Admin user sees "Something went wrong" message](/products/sport_news_portal/web_application_features/manage_news_partners/images/something_went_wrong_popup.png)

</details>

## Test cases

1. Verify the possibility to delete partner integration
2. Verify the possibility to cancel of deleting partner

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the possibility to delete partner integration**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) In the partner row, click the delete icon</br>2) Click <b>Delete</b>|1) Popover to confirm deletion appears</br>2) News partner is removed from the list. User can add new partners in the drop-down list again|

### **#2. Verify the possibility to cancel of deleting partner**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>News Partners</b> configuration page</br>- There is some partner added|1) In the partner row, click the delete icon</br>2) Click <b>Cancel</b>|1) Popover to confirm deletion appears</br>2) The news partner is still present and working|
</details>
