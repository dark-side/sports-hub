### Back to [Manage advertisements on the portal](../../) feature

# Allow admin user to configure advertisements

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure the list of advertisements  
    So that it is possible to promote them via the Sport News site

## Acceptance criteria

<pre>
<b><i>Scenario: An admin configures the list of advertisements</i></b>

Given I am logged in as an admin user

When I view the <b>Advertising</b> configuration page
Then I see the following:
  - Table with a list of available advertisements that contains ads name, status, and actions
  - Section with Advertisements’ labels and the <b>+ New Ad</b> button in the header section

When I click <b>+ New Ad</b>
Then I see the <b>Enter new Ad name</b> dialog with the <b>Name</b> input, and the <b>Cancel</b> and <b>Save</b> buttons

When I enter the name of a new ad and click <b>Save</b>
Then I see a new ad is added on the top of the ads table. Ad’s preview block is displayed on the right side of the page with a date of Ad’s creation and the configuration page which contains:
  - URL input for the advertised item
  - List of categories where advertisement should be displayed (Note: advertisement category is optional. If no category is selected, then advertisement can be shown on any page of the site)
  - Opened (the number that indicates how many times the user clicked on the advertised item, the default value for new advertisement is 0)
  - Displayed (the number that indicates how many times an advertisement is displayed on the site, the default value for the new advertisement is 0)
  - Cancel and Save buttons

When I enter the advertisement URL
Then I see an advertisement image in the preview block on the right side of the page

When I select some category for the advertisement
Then the user sees this advertisement only on those pages that are related to a specified category

When I don't select any category
Then the user sees this advertisement on any page of the site

When I click on any advertisement on the table
  And I change the status from inactive to active
Then the user sees an advertisement on the Sport News site

When I change the status from active to inactive
Then user does not see ads on the Sport News site

When I click on the edit icon
Then the form with advertisement details is opened and I can edit the advertisement

When I click delete icon
Then confirmation popup appears

When I click the <b>Yes</b> button on the confirmation popup
Then I see that the advertisement is deleted
</pre>

## Mockups

1. Admin sees Empty Page message
2. Admin sees add new ad popup
3. Admin sees new ad empty form
4. Admin sees filled in form
5. Admin sees saccess message on save
6. Admin sees a list of ads

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin sees Empty Page message:**

![Admin sees Empty Page message](/products/sport_news_portal/web_application_features/manage_ads/images/no_ads_added.png)

**2. Admin sees add new ad popup:**

![Admin sees add new ad popup](/products/sport_news_portal/web_application_features/manage_ads/images/add_new_ads_popup.png)

**3. Admin sees new ad empty form**

![Admin sees new ad empty form](/products/sport_news_portal/web_application_features/manage_ads/images/add_new_ads.png)

**4. Admin sees filled in form**

![Admin sees filled in form](/products/sport_news_portal/web_application_features/manage_ads/images/add_new_ads_filled_in_form.png)

**5. Admin sees saccess message on save**

![Admin sees saccess message on save](/products/sport_news_portal/web_application_features/manage_ads/images/ads_is_saved_popup.png)

**6. Admin sees a list of ads**

![Admin sees a list of ads](/products/sport_news_portal/web_application_features/manage_ads/images/ads_list.png)

</details>

## Test cases

1. Verify the content of the open form on the Advertising configuration page
2. Verify that admin can add new advertisement
3. Verify that admin can update new advertisement by entering data in the required fields
4. Verify changing advertisement status from inactive to active
5. Verify changing advertisement status from active to inactive
6. Verify that admin can edit an advertisement
7. Verify that admin can update an advertisement with categories to be displayed in
8. Verify that admin can delete an advertisement

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify the content of the open form on the Advertising configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page|1) Examine the content of the page|1) Table with a list of open advertisements with the following column names: Ad Name, Status, Actions and an expandable section with URL, Category, Opened, and Displayed are present|

### **#2. Verify that admin can add new advertisement**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page|1) Click the <b>+ New Ad</b> button</br>2) Enter an advertisement name</br>3) Click <b>Add</b> button|1) Popup to enter advertisement name appears</br>3) The new advertisement is displayed at the top of the advertisements table with the inactive status and opened empty boxes that need to be entered with data|

### **#3. Verify that admin can update new advertisement by entering data in the required fields**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement added|1) Open already created advertisement</br>2) In the <b>URL</b> input, enter a URL</br>3) Click <b>Save</b> button|3) The advertisement is updated with the new URL|

### **#4. Verify changing advertisement status from inactive to active**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some inactive advertisement|1) Click inactive toggle|1) Toggle changed to active. Users can see advertisements on the site|

### **#5. Verify changing advertisement status from active to inactive**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some active advertisement|1) Click active toggle|1) Toggle changed to inactive. Users can’t see advertisements on the site|

### **#6. Verify that admin can edit an advertisement**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement|1) Select an advertisement from the list, and then click the edit icon</br>2) Update the URL and picture</br>3) Click <b>Save</b> button|3) The advertisement is updated with the new data|

### **#7. Verify that admin can update an advertisement with categories to be displayed in**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement|1) Select some categories by selecting checkboxes|1) User sees the advertisement only on pages with the selected categories|

### **#8. Verify that admin can delete an advertisement**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Log in by admin account</br>- Go to the <b>Advertising</b> configuration page</br>- There is some advertisement|1) Select an advertisement from the list, and then click the delete icon</br>2) Click the <b>Yes</b> button on the confirmation popup|1) The confirmation popup appears</br>2) The advertisement is deleted|
</details>
