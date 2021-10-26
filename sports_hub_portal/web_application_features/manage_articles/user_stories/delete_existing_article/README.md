### Back to [Manage articles on the portal](../../) feature

# Allow admin users to delete an existing article

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to delete an existing article

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes an existing article</i></b>

Given I am logged in as an admin user

When I select any sports category link on the admin side
Then I see the list of blocks with articles

When I hover over any article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an article
Then I see the <b>Delete</b> menu item present

When I click the <b>Delete</b> menu item
Then I see confirmation dialog

When I click <b>Cancel</b> on the confirmation dialog
Then I see the dialog disappears and the article is still present

When I confirm deleting
Then I see a success message
  And the article is removed from the list
</pre>

## Mockups

1. Admin user sees <b>Delete</b> among actions for the article
2. Admin user sees a delete confirmation dialog

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees Delete among actions for the article:**

![Admin user sees Delete among actions for the article](/sports_hub_portal/web_application_features/manage_articles/images/published_article_actions.png)

**2. Admin user sees a delete confirmation dialog:**

![Admin user sees a delete confirmation dialog](/sports_hub_portal/web_application_features/manage_articles/images/delete_article_confirmation.png)

</details>

## Test cases

1. Verify that admin is able to delete an unpublished article
2. Verify that admin is able to delete a published article
3. Verify that admin is able to cancel deleting of any article

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify that admin is able to delete an unpublished article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) On the confirmation popover, click <b>Yes</b>|3) A success message is shown and article is deleted from the list|

### **#2. Verify that admin is able to delete a published article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is a published article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) On the confirmation popover, click <b>Yes</b>|3) A success message is shown and article is deleted from the list|

### **#3. Verify that admin is able to cancel deleting of any article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the category configuration page</br>- There is a published article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) On the confirmation popover, click <b>Cancel</b>|3) The article is present in the list|

</details>
