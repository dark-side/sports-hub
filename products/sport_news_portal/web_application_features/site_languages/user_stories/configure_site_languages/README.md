### Back to [Site Languages on the portal](../../) feature

# Allow admin user to configure site languages on the portal

- [Description](#description)
- [Acceptance criteria](#acceptance-criteria)
- [Mockups](#mockups)
- [Test cases](#test-cases)

## Description

    As an admin user
    I want to configure a list of available site languages 
    So user can select the preferred language for the Sport News site

## Acceptance criteria

<pre>
Scenario: An admin user configures the list of available site languages
Given I am logged in as an admin user

When I view the <b>Languages</b> configuration page
Then I see a table with the list of languages available for the Sport News site and a language status toggle

When I hover over some language
Then I see the <b>Delete</b> icon

When I click on the <b>Delete</b> icon
Then I see the language is deleted from the list

When I hover over the English language
Then I do not see the Delete icon

When I switch the language status toggle (<i>present for any language except English</i>)
Then I see the language is activated or deactivated
<i>Note: When language is in the deactivated state, it’s not shown in the drop-down list with site languages in the site header</i>

When I view the Language configuration page
Then in the upper-right corner of the page, I see the <b>New Language</b> button

When I click <b>New Language</b>
Then I see the <b>Add Language</b> pop-up window with the multi-select input with checkboxes, the <b>Add</b> and <b>Cancel</b> buttons

When I select the list of languages that I want to make available on the site and click <b>Add</b>
Then I see new languages are displayed in the languages list

When I click the <b>Cancel</b> button in the <b>Add Language</b> pop-up window
Then I see the pop-up window is closed and no new languages appear in the language list
</pre>

## Mockups

1. Admin user sees configaration site languages page
2. Admin user sees "Add Language" popup
3. Admin user sees successful saved message
4. Admin user sees select language drop-down

<details>
  <summary>Click here to see mockups details</summary>

**1. Admin user sees configaration site languages page:**

![Admin user sees configaration site languages page](/products/sport_news_portal/web_application_features/site_languages/images/configaration_site_languages.png)

**2. Admin user sees "Add Language" popup:**

!["Add Language" popup](/products/sport_news_portal/web_application_features/site_languages/images/add_language_popup.png)

**3. Admin user sees successful saved message:**

![Admin user sees successful saved message](/products/sport_news_portal/web_application_features/site_languages/images/languages_saved_message.png)

**4. Admin user sees select language drop-down:**

![Admin user sees select language drop-down](/products/sport_news_portal/web_application_features/site_languages/images/admin_selects_language.png)

</details>

## Test cases

1. Verify content of the Languages configuration page
2. Verify that it is possible to delete the language
3. Verify that it is not possible to delete English language
4. Verify that it is possible to activate/deactivate the language
5. Verify that it is not possible to deactivate English language
6. Verify the New Language button functionality
7. Verify that it is possible to cancel the adding of a new language

<details>
  <summary>Click here to see test cases details</summary>

### **#1. Verify content of the Languages configuration page**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Examine the content of the <b>Languages</b> configuration page|1) There is a table with the list of languages available for the Sport News site users and the Status toggle is present for each language except English|

### **#2. Verify that it is possible to delete the language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Hover over any language except English</br>2) Click <b>Delete</b>|1) The <b>Delete</b> button appears</br>2) The language is deleted from the list. The language is unavailable, the user can not select it|

### **#3. Verify that it is not possible to delete English language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Hover over English language</br>2) Examine the page|2) The <b>Delete</> button is not shown|

### **#4. Verify that it is possible to activate/deactivate the language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Hover over any language with the <b>Active</b> status</br>2) Switch the status toggle</br>3) Hover over any language with the <b>Inactive</b> status</br>4) Switch the status toggle|2) The language is deactivated and is unavailable for the users to be selected</br>4) The language is activated and is available for the users to be selected|

### **#5. Verify that it is not possible to deactivate English language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Hover over English language</br>2) Examine the page|2) There is no Status toggle for English language|

### **#6. Verify the New Language button functionality**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Click <b>+New Language</b></br>2) From the list of languages, select new languages</br>3) Click <b>Add</b>|3) The new languages are displayed in the languages list and are enabled by default|

### **#7. Verify that it is possible to cancel the adding of a new language**

|Preconditions|Steps|Expected result
--------------|-----|----------
|- Go to Sport News home page</br>- Log in by admin account</br>- Go to the <b>Languages</b> configuration page|1) Click <b>+New Language</b></br>2) From the list of languages, select new languages</br>3) Click <b>Cancel</b>|3) The Add language pop-up window is closed and no new language appears in the table|
</details>
