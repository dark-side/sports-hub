### Back to [Lifestyle and Dealbook news](../../) feature

# Allow admin users to delete Lifestyle and Dealbook's articles

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to delete existing articles in Lifestyle and Dealbook

## Acceptance criteria

<pre>
<b><i>Scenario: An admin user deletes an existing article</i></b>

Given I am logged in as an admin user

When I select the <b>Lifestyle</b> or <b>Dealbook</b> link on the admin side
Then I see the list of blocks with articles

When I hover over an any article
Then I see the ellipsis (<b>...</b>) button in the upper-right corner

When I click "<b>...</b>" the menu icon for an article
Then I see the <b>Delete</b> menu item is present

When I select <b>Delete</b> menu item
Then I see confirmation dialog

When I cancel deleting of the article
Then I see the dialog disappears and article is still present

When I confirm deleting of the article
Then I see a success message
  And the article is removed from the list
</pre>

## Mockups

1. Admin user sees a confirmation pop-up window to delete the article

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees a confirmation pop-up window to delete the article:**

![Admin user sees a confirmation pop-up window to delete the article](/products/sport_news_portal/web_application_features/lifestyle_dealbook_news/images/confirmation_to_delete.png)

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
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) Confirm deleting on the confirmation popover|3) A success message is shown and the article is deleted from the list|

### **#2. Verify that admin is able to delete a published article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is a published article|1) Hover over a published article</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) Confirm deleting on the confirmation popover|3) A success message is shown and the article is deleted from the list|

### **#3. Verify that admin is able to cancel deleting of any article**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to <b>Lifestyle</b> and <b>Dealbook</b></br>- There is an unpublished article|1) Hover over an unpublished article</br>2) Click "<b>...</b>" button > <b>Delete</b> menu item</br>3) Cancel deleting on the confirmation popover|3) The article is present in the list|
</details>
