### Back to [Manage advertisements on the portal](../../) feature

# Allow admin user to configure advertisements

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure the list of advertisements
    So that it is possible to promote them via the Sports Hub site

## Acceptance criteria

<pre>
<b><i>Scenario: An admin configures the list of advertisements</i></b>

Given I am logged in as an admin user

When I view the <b>Advertising</b> configuration page
Then I see the following:
  - Table with a list of available advertisements that contains ads name, status, and actions
  - Section with advertisements’ labels and the <b>+ New Ad</b> button in the header section

When I click <b>+ New Ad</b>
Then I see the <b>Enter new Ad name</b> dialog with the <b>Name</b> input, and the <b>Cancel</b> and <b>Save</b> buttons

When I enter the name of a new ad and click <b>Save</b>
Then I see a new ad is added on the top of the ads table. Ad’s preview block is displayed on the right side of the page with a date of Ad’s creation and the configuration page which contains:
  - URL input for the advertised item
  - List of categories where advertisement should be displayed (Note: advertisement category is optional. If no category is selected, then advertisement can be shown on any page of the site)
  - <b>Opened</b> (the number that indicates how many times the user selected the advertised item, the default value for new advertisement is 0)
  - <b>Displayed</b> (the number that indicates how many times an advertisement is displayed on the site, the default value for the new advertisement is 0)
  - <b>Cancel</b> and <b>Save</b> buttons

When I enter the advertisement URL
Then I see an advertisement image in the preview block on the right side of the page

When I select some category for the advertisement
Then the user sees this advertisement only on those pages that are related to a specified category

When I don't select any category
Then the user sees this advertisement on any page of the site

When I select any advertisement on the table
  And I change the status from inactive to active
Then the user sees an advertisement on the Sports Hub site

When I change the status from active to inactive
Then user does not see ads on the Sports Hub site

When I click the edit icon
Then the form with advertisement details is opened and I can edit the advertisement

When I click the delete icon
Then confirmation pop-up window appears

When I click the <b>Yes</b> button on the confirmation pop-up window
Then I see that the advertisement is deleted
</pre>

## Mockups

1. Admin sees Empty page message
2. Admin sees add new ad pop-up window
3. Admin sees new ad empty form
4. Admin sees filled in form
5. Admin sees success message on save
6. Admin sees a list of ads

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin sees Empty page message:**

![Admin sees Empty page message](/sports_hub_portal/web_application_features/manage_ads/images/no_ads_added.png)

**2. Admin sees add new ad pop-up window:**

![Admin sees add new ad pop-up window](/sports_hub_portal/web_application_features/manage_ads/images/add_new_ads_popup.png)

**3. Admin sees new ad empty form**

![Admin sees new ad empty form](/sports_hub_portal/web_application_features/manage_ads/images/add_new_ads.png)

**4. Admin sees filled in form**

![Admin sees filled in form](/sports_hub_portal/web_application_features/manage_ads/images/add_new_ads_filled_in_form.png)

**5. Admin sees success message on save**

![Admin sees success message on save](/sports_hub_portal/web_application_features/manage_ads/images/ads_is_saved_popup.png)

**6. Admin sees a list of ads**

![Admin sees a list of ads](/sports_hub_portal/web_application_features/manage_ads/images/ads_list.png)

</details>

## Test cases

1. Verify the content of the opened form on the <b>Advertising</b> configuration page
2. Verify that admin can add a new advertisement
3. Verify that admin can update a new advertisement by entering data in the required fields
4. Verify the possibility of changing advertisement status from <b>Inactive</b> to <b>Active</b>
5. Verify the possibility of changing advertisement status from <b>Active</b> to <b>Inactive</b>
6. Verify that admin can edit an advertisement
7. Verify that admin can update an advertisement with categories to be displayed in
8. Verify that admin can delete an advertisement

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the opened form on the Advertising configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page|1) Examine the content of the page|1) Table with a list of opened advertisements with the following column names: Ad Name, Status, Actions, an expandable section with URL, Category, Opened, and Displayed is present|

### **#2. Verify that admin can add a new advertisement**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page|1) Click the <b>+ New Ad</b> button</br>2) Enter an advertisement name</br>3) Click <b>Add</b>|1) Pop-up window to enter advertisement name appears</br>3) The new advertisement is displayed at the top of the advertisements table with the <b>Inactive</b> status and opened empty boxes that need to be entered with data|

### **#3. Verify that admin can update a new advertisement by entering data in the required fields**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement added|1) Open already created advertisement</br>2) In the <b>URL</b> input, enter a URL</br>3) Click <b>Save</b>|3) The advertisement is updated with the new URL|

### **#4. Verify the possibility of changing advertisement status from Inactive to Active**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some inactive advertisement|1) Click the <b>Inactive</b> toggle|1) The toggle changes to <b>Active</b>. Users can see advertisements on the site|

### **#5. Verify the possibility of changing advertisement status from Active to Inactive**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some active advertisement|1) Click the <b>Active</b> toggle|1) The toggle changes to <b>Inactive</b>. Users can’t see advertisements on the site|

### **#6. Verify that admin can edit an advertisement**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement|1) Select an advertisement from the list, and then click the edit icon</br>2) Update the URL and picture</br>3) Click <b>Save</b>|3) The advertisement is updated with the new data|

### **#7. Verify that admin can update an advertisement with categories to be displayed in**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement|1) Select some categories by selecting checkboxes|1) The user sees the advertisement only on pages with the selected categories|

### **#8. Verify that admin can delete an advertisement**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in with admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement|1) Select an advertisement from the list, and then click the delete icon</br>2) Click the <b>Yes</b> button on the confirmation pop-up window|1) The confirmation pop-up window appears</br>2) The advertisement is deleted|
</details>
